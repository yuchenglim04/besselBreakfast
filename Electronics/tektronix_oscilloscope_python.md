https://github.com/tektronix/Programmatic-Control-Examples/blob/master/Examples/Oscilloscopes/BenchScopes/src/SimplePlotExample/tbs_simple_plot.py

https://github.com/tektronix/Programmatic-Control-Examples/blob/master/Examples/Oscilloscopes/BenchScopes/src/SaveHardcopyExample/SaveHardcopy_example.py

```
import time # std module
import pyvisa as visa 
```
```
visa_address = 'USB0::0x0699::0x03C4::C026212::INSTR'

rm = visa.ResourceManager()
scope = rm.open_resource(visa_address)
scope.timeout = 20000                                         # ms ; scope will not reply queries immediately. So how much time 
                                                              # you will wait before error message appears
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
scope.write('autoset EXECUTE') # autoset
t3 = time.perf_counter()
r = scope.query('*opc?') # sync
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

scope.write('data:start 1')                               # first sample in memory
record = int(scope.query('wfmpre:nr_pt?'))
scope.write('data:stop {}'.format(record)) # last sample
scope.write('wfmpre:byt_nr 1')                               # 1 byte per sample
```



```
scope.close()
rm.close()
```
