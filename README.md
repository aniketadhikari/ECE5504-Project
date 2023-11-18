# ECE5504 Final Project
Codebase for my final project in ECE 5504 Computer Architecture
# Evaluation Metrics 
The project (25%) evaluation contains three parts:
1. proposal (5%)
2. presentation (5%)
3. report (15%)

The project will be evaluated by 
1. whether the idea/design makes sense and contributes to a better
computer architecture design
2. whether the evaluation results are solid
3. whether the presentation and write-up explain the ideas and results clearly.

# Goal: Optimize Architecture Configurations for Specific Applications 
In this type of project, you work with existing implementations, however, you want to optimize the architecture configuration for your application.
## Parameters Available for Manipulation ( > 5)
Study at least 5 different parameters in the configuration and find a methodology to find the optimal design for your application.
1. decodeWidth (WithNSmallBooms = 1, WithNMediumBooms = 2, WithNLargeBooms = 3)
2. numIntPhysRegisters
3. fetchWidth
4. numRobEntries
5. numIntPhysRegisters
6. numFpPhysRegisters
7. numLdqEntries
8. numStqEntries
9. maxBrCount
10. numFetchBufferEntries
11. nPerfCounters
12. FtqParameters
13. DCacheParams
    - nSets
    - nWays
    - nMSHRs
    - nTLBWays
15. ICacheParams
    - nSets
    - nWays
    - fetchBytes
16. Branch Prediction Technique
    - None
    - TAGE
    - SW
    - GShare
    - Alpha
## Evaluation Metrics (1-2)
* CPI
* Cache hit rate 
## Evaluation Platform
- RISC-V BOOM core
## Evaluation Benchmarks (1-5)
* [Median](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/median/median_main.c)
  * This benchmark performs a 1D three element median filter
* [Dhrystone](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/dhrystone/dhrystone_main.c)
  * This is the classic Dhrystone synthetic integer benchmark.
* [Multi-threaded Matrix Multiply benchmark (mt-matmul)](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/mt-matmul/mt-matmul.c) 
  * This benchmark multiplies two 2-D arrays together and writes the results to a third vector
* [QSort](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/qsort/qsort_main.c)
  * This benchmark uses quicksort to sort an array of integers.
* [RSort](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/rsort/rsort.c)
  * Similar to QSort, except it does the reverse, meaning it sorts from greatest to least 
* [Towers of Hanoi (towers_main)](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/towers/towers_main.c)
  * Towers of Hanoi is a classic puzzle problem. The game consists of three pegs and a set of discs. Each disc is a different size, and initially all of the discs are on the left most peg with the smallest disc on top and the largest disc on the bottom. The goal is to move all of the discs onto the right most peg. The catch is that you are only allowed to move one disc at a time and you can never place a larger disc on top of a smaller disc.
* [Vector-vector Add Benchmark (vvadd_main)](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/vvadd/vvadd_main.c)
  * This benchmark uses adds to vectors and writes the results to a third vector.
* [Memcpy](https://github.com/riscv-software-src/riscv-tests/blob/master/benchmarks/memcpy/memcpy_main.c)
  * This benchmark tests the memcpy implementation
## Location and Meaning of Config Files 
Rocket Config:
```
~/rocket/chipyard-clean/generators/chipyard/src/main/scala/config/RocketConfigs.scala
```
b. Rocket-chip core config:
```
~/rocket/chipyard-clean/generators/rocket-chip/src/main/scala/subsystem/Configs.scala
```
c. BOOM configs:
```
~/rocket/chipyard-clean/generators/chipyard/src/main/scala/config/BoomConfigs.scala
```
d. BOOM core configs:
```
~/rocket/chipyard-clean/generators/boom/src/main/scala/common/config-mixins.scala
```
