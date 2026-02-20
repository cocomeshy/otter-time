# time

Cross-platform time and clock utilities for Otter.

## Exports

- `now()` → Unix epoch timestamp in seconds
- `now_ms()` → Unix epoch in milliseconds
- `monotonic_ms()` → Monotonic clock in milliseconds
- `monotonic_ns()` → High-resolution monotonic nanoseconds
- `sleep(ms)` → Suspend thread for N milliseconds
- `elapsed_ms(start)` → Elapsed time since start timestamp
- `hour(epoch)` → Hour (0-23) from epoch
- `minute(epoch)` → Minute (0-59) from epoch
- `second(epoch)` → Second (0-59) from epoch
- `weekday(epoch)` → Day of week (0=Mon, 6=Sun)

## Install

```
otter pkg add time 1.0.0
otter pkg pull
```

## Usage

```otter
use time;
use io;

~> main() -> void {
  rock start:int = time.monotonic_ms();
  time.sleep(100);
  rock elapsed:int = time.elapsed_ms(start);
  io.out("elapsed ms:");
}
```
