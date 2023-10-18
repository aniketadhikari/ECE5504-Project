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
1. `Param1`
2. `Param2`
3. `Param3`
4. `Param4`
5. `Param5`
## Evaluation Metrics (1-2)
* CPI
* Cache hit rate 
## Evaluation Platform
- RISC-V BOOM core
- RISC-V Rocket core
## Evaluation Benchmarks (1-5)
* Drystone.riscv 
* Qsort.riscv
* multiplication.riscv
## Location of Config Files 
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
