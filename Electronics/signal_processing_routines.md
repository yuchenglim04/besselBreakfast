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

