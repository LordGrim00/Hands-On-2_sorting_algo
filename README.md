# DAA Hands On-2

## Argue Selection Sort Correctness

To demonstrate that the selection sort algorithm is correct, we need to establish three aspects of a loop invariant.

  - **Initialize**
  - **Maintenance**
  - **Termination** 

### 1. Initialization (Base Case):
Before the first iteration (i = 0), the subarray arr`[0:0]` is empty, which trivially satisfies the loop invariant. Hence, the loop invariant holds before the first iteration.

### 2. Maintenance (Inductive Step):
Assume that the loop invariant holds at the start of the `i`-th iteration. During this iteration, the algorithm selects the smallest element from the unsorted portion of the array `(arr[i:n])` and swaps it with the element at index `i`. After the swap, the subarray `arr[0:i+1]` will contain the smallest `i+1` elements in sorted order because:
The subarray `arr[0:i]` was already sorted by the induction hypothesis.
The newly placed element `arr[i]` is the smallest element from `arr[i:n]`, so the subarray `arr[0:i+1]` is sorted.
Thus, the loop invariant is maintained at the end of each iteration.

### 3. Termination (Final Case):
The algorithm terminates when `i = n`, at which point the entire array is sorted. Since the loop invariant holds at each iteration, by the time the loop finishes, the entire array `arr[0:n]` must be sorted.

## Benchmarking the Runtime of Each Algorithm

Your benchmarks should include information about your computer (RAM, CPU, etc.) and be run with various input sizes, from small (array of size 5, 10, 20) all the way up to large arrays (where your computer is struggling). Below is a plot of time vs input size `n`.

### System Information:
- **Platform:** Darwin 20.6.0
- **Processor:** i386
- **RAM:** 8.00 GB
- **Python Version:** 3.8.9
- **ROM:** 465.57 GB

### Benchmarks

- Bubble Sort - Input Size: 5, Time Taken: 0.000008 seconds
- Bubble Sort - Input Size: 10, Time Taken: 0.000014 seconds
- Bubble Sort - Input Size: 20, Time Taken: 0.000045 seconds
- Bubble Sort - Input Size: 50, Time Taken: 0.000263 seconds
- Bubble Sort - Input Size: 100, Time Taken: 0.001033 seconds
- Bubble Sort - Input Size: 200, Time Taken: 0.003278 seconds
- Bubble Sort - Input Size: 500, Time Taken: 0.030660 seconds
- Bubble Sort - Input Size: 1000, Time Taken: 0.118672 seconds
- Bubble Sort - Input Size: 2000, Time Taken: 0.522428 seconds
- Bubble Sort - Input Size: 5000, Time Taken: 3.119597 seconds
- Insertion Sort - Input Size: 5, Time Taken: 0.000007 seconds
- Insertion Sort - Input Size: 10, Time Taken: 0.000011 seconds
- Insertion Sort - Input Size: 20, Time Taken: 0.000020 seconds
- Insertion Sort - Input Size: 50, Time Taken: 0.000096 seconds
- Insertion Sort - Input Size: 100, Time Taken: 0.000393 seconds
- Insertion Sort - Input Size: 200, Time Taken: 0.001617 seconds
- Insertion Sort - Input Size: 500, Time Taken: 0.015599 seconds
- Insertion Sort - Input Size: 1000, Time Taken: 0.059270 seconds
- Insertion Sort - Input Size: 2000, Time Taken: 0.199300 seconds
- Insertion Sort - Input Size: 5000, Time Taken: 1.289965 seconds
- Selection Sort - Input Size: 5, Time Taken: 0.000012 seconds
- Selection Sort - Input Size: 10, Time Taken: 0.000016 seconds
- Selection Sort - Input Size: 20, Time Taken: 0.000035 seconds
- Selection Sort - Input Size: 50, Time Taken: 0.000110 seconds
- Selection Sort - Input Size: 100, Time Taken: 0.000383 seconds
- Selection Sort - Input Size: 200, Time Taken: 0.003373 seconds
- Selection Sort - Input Size: 500, Time Taken: 0.018062 seconds
- Selection Sort - Input Size: 1000, Time Taken: 0.058779 seconds
- Selection Sort - Input Size: 2000, Time Taken: 0.182926 seconds
- Selection Sort - Input Size: 5000, Time Taken: 1.605420 seconds

![Figure_1](https://github.com/user-attachments/assets/78a57dc5-06dc-45c0-a5fb-562b4206dd8f)

