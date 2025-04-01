## Test results

### Apple M3 Max

```
❯ npm run benchmark 

> dd-trace-vitest-debug@1.0.0 benchmark
> hyperfine --warmup 5 'npm run jest-without-dd-trace' 'npm run vitest-without-dd-trace' 'npm run jest-with-dd-trace' 'npm run vitest-with-dd-trace'

Benchmark 1: npm run jest-without-dd-trace
  Time (mean ± σ):     333.8 ms ±   1.3 ms    [User: 272.9 ms, System: 49.4 ms]
  Range (min … max):   331.4 ms … 335.1 ms    10 runs
 
Benchmark 2: npm run vitest-without-dd-trace
  Time (mean ± σ):     471.7 ms ±   5.9 ms    [User: 1435.6 ms, System: 336.0 ms]
  Range (min … max):   462.1 ms … 483.1 ms    10 runs
 
Benchmark 3: npm run jest-with-dd-trace
  Time (mean ± σ):     895.4 ms ±   7.1 ms    [User: 586.1 ms, System: 238.3 ms]
  Range (min … max):   885.8 ms … 903.8 ms    10 runs
 
Benchmark 4: npm run vitest-with-dd-trace
  Time (mean ± σ):      2.052 s ±  0.024 s    [User: 10.495 s, System: 2.688 s]
  Range (min … max):    2.015 s …  2.096 s    10 runs
 
Summary
  npm run jest-without-dd-trace ran
    1.41 ± 0.02 times faster than npm run vitest-without-dd-trace
    2.68 ± 0.02 times faster than npm run jest-with-dd-trace
    6.15 ± 0.08 times faster than npm run vitest-with-dd-trace
```
