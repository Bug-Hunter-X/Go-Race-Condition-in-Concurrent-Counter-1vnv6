# Go Race Condition in Concurrent Counter

This repository demonstrates a common race condition in Go programs that use goroutines to increment a counter.  The program attempts to increment a counter using multiple goroutines concurrently without proper synchronization mechanisms. This leads to an unpredictable and often incorrect final count.

The `bug.go` file contains the buggy code. The `bugSolution.go` file provides a corrected version using a mutex to protect the shared counter.

## How to run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your_username>/go-race-condition.git
   ```
2. Navigate to the repository directory:
   ```bash
   cd go-race-condition
   ```
3. Run the buggy code:
   ```bash
   go run bug.go
   ```
4. Observe the inconsistent and incorrect final count.
5. Run the corrected code:
   ```bash
   go run bugSolution.go
   ```
6. Observe the consistent and correct final count.

## Learning Points

This example highlights the importance of proper synchronization when dealing with shared resources across multiple goroutines in Go.  Using `sync.Mutex` or other synchronization primitives is crucial to prevent data races and ensure the correctness of concurrent programs.