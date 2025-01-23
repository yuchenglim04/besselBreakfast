https://github.com/tektronix/Programmatic-Control-Examples/blob/master/Examples/Oscilloscopes/BenchScopes/src/SimplePlotExample/tbs_simple_plot.py

https://github.com/tektronix/Programmatic-Control-Examples/blob/master/Examples/Oscilloscopes/BenchScopes/src/SaveHardcopyExample/SaveHardcopy_example.py

```
import time                                               # std module
import pyvisa as visa 
```
```
visa_address = 'USB0::0x0699::0x03C4::C026212::INSTR'

rm = visa.ResourceManager()
scope = rm.open_resource(visa_address)
scope.timeout = 20000                                    # ms ; scope will not reply queries immediately.
                                                         # Sets much time  before error message appears
scope.encoding = 'latin_1'
scope.read_termination = '\n'
scope.write_termination = None
scope.write('*cls') # clear ESR

print(scope.query('*idn?'))

input("""
ACTION:
Connect probe to oscilloscope Channel 1 and the probe compensation signal.

Press Enter to continue...
""")

```

```
scope.write('autoset EXECUTE')                         # autoset
t3 = time.perf_counter()
r = scope.query('*opc?')                               # sync; scope reply '1' after operation done
t4 = time.perf_counter()
print('autoset time: {} s'.format(t4 - t3))
```

```
# io config
scope.write('header 0')                                  # 0 = OFF; omit headers from query responses.
scope.write('data:encdg RIBINARY')

scope.write('CH2:probe 1')                               # 1x attenuation
scope.write('CH2:scale 100E-3')                                #100mV / div
scope.write('CH2:position 11')                              # offset by 11 div , i.e. 11*100mV

scope.write('horizontal:main:scale 100E-6')                # 100 micro seconds

scope.write('data:start 1')                                   # 1st sample in memory; doesn't start from 0!
n_samples = int(scope.query('wfmpre:nr_pt?'))
scope.write('data:stop {}'.format(n_samples)) # last sample
scope.write('wfmpre:byt_nr 1')                               # 1 byte per sample
```

```
#get output
# acquire waveform; store in scope
scope.write('data:source CH1')                               # choose channel 1
scope.write('acquire:state 0')                               # stop
scope.write('acquire:stopafter SEQUENCE')                     # single
scope.write('acquire:state 1')                               # run

t5 = time.perf_counter()
r = scope.query('*opc?') # sync
t6 = time.perf_counter()
print('acquire time: {} s'.format(t6 - t5))

# data transfer from scope to computer
t7 = time.perf_counter()
bin_wave = scope.query_binary_values('curve?', datatype='b', container=np.array)
t8 = time.perf_counter()
print('transfer time: {} s'.format(t8 - t7))

# retrieve scaling factors
tscale = float(scope.query('wfmpre:xincr?'))                                      # x increment
tstart = float(scope.query('wfmpre:xzero?'))                                      # value of x_0
vscale = float(scope.query('wfmpre:ymult?'))                                       # y multiplier; volts / div
voff = float(scope.query('wfmpre:yzero?'))                                   # reference/offset voltage (volts)               
vpos = float(scope.query('wfmpre:yoff?'))                                    # digitizer offset/reference position (div)

# error checking
r = int(scope.query('*esr?'))
print('event status register: 0b{:08b}'.format(r))
r = scope.query('allev?').strip()
print('all event messages: {}'.format(r))

# create scaled vectors
# horizontal (time)
total_time = tscale * n_samples
tstop = tstart + total_time
scaled_time = np.linspace(tstart, tstop, num=n_samples, endpoint=True, dtype='double')
                                                                      # includes first&last samples (endpoint) 
# vertical (voltage)
unscaled_wave = np.array(bin_wave, dtype='double')                                         # data type conversion
scaled_wave = (unscaled_wave - vpos) * vscale + voff

```

```
scope.close()
rm.close()
```
