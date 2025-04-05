# HPX Matrix Multiplication (Async Version)

This project implements **matrix multiplication** using the [HPX](https://hpx.stellar-group.org/) C++ parallel runtime system. Instead of using traditional parallel loop constructs, this version leverages **fine-grained asynchronous tasks** via `hpx::async` for each row of the result matrix.

---


## Features

Unlike the more common HPX implementation using `hpx::experimental::for_loop` with a parallel execution policy, this version:

- Spawns a **separate asynchronous task per row** using `hpx::async`
- Provides **fine-grained task-level parallelism**
- Gives more control over task creation, scheduling, and futures

---

## Build Instructions

```bash
# Clone the repo
git clone git@github.com:kylehaokunwu/HPX-matrix-multiplication.git
cd HPX-matrix-multiplication

# Create a build directory
mkdir build && cd build

# Run CMake
cmake ..

# Build the executable
make

```
---
## Example Output
```bash
kyle@MacBookPro:~/Desktop/cs_projects/hpxTest/build$ ./matrix_mul 
using seed: 2115157462

Matrix A is:
0 2 10 
4 3 3 

Matrix B is:
0 2 
10 4 
3 3 

Matrix R is:
50 38 
39 29
