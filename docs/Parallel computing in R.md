<!--
---

[TOC]
-->
---

**Foreword**

Code snippets and notes.

---

# Use of parallel computing

R uses in-memory calculations. All data need to be processed in the random-access memory (RAM). It is highly efficient and rapid, but can be burdensome as the size of the data increase and the RAM becomes limited. 

R is a single-threaded program. In the modern multi-core processors, R cannot effectively use all the computing cores. Even though a CPU had 260 computing core, R would only take 1/260 of the computing power!

We can distribute the task on multiple machines (multiple CPU-cache-RAM) and use several parallel single-threaded computations.

## Applications

- Linear algebra transformations.
- Bootstrapping, Monte Carlo, inferential computations.
- Using the `caret` package.
- cross-validation in machine learning (train-test sets).
- SVD.
- PCA.
- LDA.
- regressions with a binary or multinomial dependent variables.
- Neural networks and deep learning.

# Implicit mode

It is the most suitable mode. It requires some investment in hardware and specialized packages.

Nowadays, it can be done in the cloud with no initial investment. Cloud computing is highly scalable (in terms of capacity and cost).

# Explicit mode

We have to deal with more details: partition data, distribute tasks, collect results, etc. Some might prefer this control over the operations.

It can be done with a simple laptop on 4 cores for example. On Linux, with 4 cores, tests demonstrated that computations were 3 times faster than on a single thread. We can also build a cluster by bridging two or more machine together to add up more cores. One machine becomes the master and the other machines become the slave.

## Functions

We can use the `apply` family functions alone.

## Packages

- `data.table`.
- `snowfall`.
- `parallel`, `doParallel`.
- `Rmpi`.
- `foreach`.
- `Multicore` on Unix-based OS.
- `RevoScaleR` with `MicrosoftML` ([doc](https://docs.microsoft.com/en-us/machine-learning-server/r-reference/revoscaler/revoscaler)).
- and others.

## Tests

With the `apply` functions, the `parallel` package, the `foreach` and `doParallel` package and [more](https://www.r-bloggers.com/how-to-go-parallel-in-r-basics-tips/).

## Implementation 1

Using the `parallel` package, then the `doParallel` and `foreach` package.

[Using a solver function](http://www.parallelr.com/r-with-parallel-computing/).

## Implementation 2

Using the `parallel` package.

Running a [binomial regression](http://www.win-vector.com/blog/2016/01/parallel-computing-in-r/).
