# quantum_code

## 环境

青果语言：[Quingo-runtime: Quingo编程框架的运行时系统，可提供使用Quingo进行量子-经典异构编程的能力。 该编程框架组织、管理系统可用的量子-经典计算资源。量子计算物理系统或量子模拟器可通过继承相关类接入此框架中。 (gitee.com)](https://gitee.com/quingo/quingo-runtime)

quingo的库中有传统计算机模拟量子环境的包

量子计算云平台：[量子计算云平台 (quantumcomputer.ac.cn)](https://quantumcomputer.ac.cn/index.html)

部署了部署了quingo和qcis两种编程语言，底层指令集用的是GCIS，提供12bit的真量子计算机，但是用的人很多，需要排队，推荐用模拟环境

## 量子计算基础

### 量子位（量子比特）




### 量子编码


#### 为什么用少量量子比特就能编码较大量的数据？

### 量子门电路

### 量子计算的指数加速

#### 量子计算的并行加速和GPU的并行加速的区别

### 量子编程环境

## 国产

国产量子编程语言：

- quingo（同时支持eQASM指令集和QCIS指令集）
- isq-core（只支持eQASM）

国产量子计算机指令集：
- QCIS

国产量子计算云平台：[科大国盾](https://quantumcomputer.ac.cn/index.html)

目前仅有12比特的真量子计算机

## 其他

IBM的量子计算机平台：https://lab.quantum-computing.ibm.com

资料丰富，需要科学上网，使用的是OpenQASM语言，编程框架为Qiskit

Azure的量子计算平台：[Azure Quantum - 量子云计算服务 | Microsoft Azure](https://azure.microsoft.com/zh-cn/products/quantum/)

包括在Azure的选项中，似乎提供一个月试用期，用的语言是Q#，可以在visual studio下载扩展获得

