## Test results

### Apple M3 Max

```
❯ node --version
v22.13.0

❯ npm run benchmark 

> dd-trace-vitest-debug@1.0.0 benchmark
> hyperfine --warmup 5 'npm run jest-without-dd-trace' 'npm run vitest-without-dd-trace' 'npm run jest-with-dd-trace' 'npm run vitest-with-dd-trace'

Benchmark 1: npm run jest-without-dd-trace
  Time (mean ± σ):     329.4 ms ±   2.2 ms    [User: 270.3 ms, System: 46.9 ms]
  Range (min … max):   326.5 ms … 333.8 ms    10 runs

Benchmark 2: npm run vitest-without-dd-trace
  Time (mean ± σ):     455.3 ms ±   8.0 ms    [User: 1427.1 ms, System: 320.0 ms]
  Range (min … max):   439.8 ms … 468.6 ms    10 runs

Benchmark 3: npm run jest-with-dd-trace
  Time (mean ± σ):     371.6 ms ±   1.8 ms    [User: 320.3 ms, System: 54.8 ms]
  Range (min … max):   369.4 ms … 375.7 ms    10 runs

Benchmark 4: npm run vitest-with-dd-trace
  Time (mean ± σ):      1.364 s ±  0.018 s    [User: 8.172 s, System: 1.391 s]
  Range (min … max):    1.332 s …  1.385 s    10 runs

Summary
  npm run jest-without-dd-trace ran
    1.13 ± 0.01 times faster than npm run jest-with-dd-trace
    1.38 ± 0.03 times faster than npm run vitest-without-dd-trace
    4.14 ± 0.06 times faster than npm run vitest-with-dd-trace
```
