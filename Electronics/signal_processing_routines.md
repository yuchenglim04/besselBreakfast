Here is a big list of useful, small code snippets. Just copy, paste to run! Only need to change the parameter at the top (sometimes perhaps copy your variable name and paste it in...)

**Simple moving average, n points**

P.S. the array notation [:-j] present problems when j is 0.

```
n = 3

smoothed_wave = np.copy(raw_wave[n-1:])

for i in range(n-1):
    smoothed_wave += raw_wave[i:-(n-1)+i]

smoothed_wave = smoothed_wave/n
```
```
n = 3

smoothed_wave = np.zeros(raw_wave.shape[0]-(n-1))

for i in range(n):
    smoothed_wave += raw_wave[i:raw_wave.shape[0]-(n-1)+i]

smoothed_wave = smoothed_wave/n
```

**Simple Autocorrelation**  
Theoretical autocorrelation is suitable for infinite, periodic, continuous functions. Our function is periodic, however we only have finite number of data points. As correlation proceeds, the overlap gets smaller and smaller and the autocorrelation function decreases in value. So we normalize each value by dividing by the number of data points. 

```
autocorrelation = []
num_elem = raw_wave.shape[0]

for x in range(num_elem):
    autocorrelation.append(np.sum(raw_wave[:num_elem-x]*raw_wave[x:])/(num_elem-x))

autocorrelation = np.array(autocorrelation)
```