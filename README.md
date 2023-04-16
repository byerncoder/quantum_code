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

#### 国产

国产量子编程语言：

- quingo（同时支持eQASM指令集和QCIS指令集）
- isq-core（只支持eQASM）

国产量子计算机指令集：
- QCIS

国产量子计算云平台：

目前仅有12比特的真量子计算机

#### 其他

IBM的量子计算机平台：https://lab.quantum-computing.ibm.com

资料丰富，需要科学上网，使用的是OpenQASM语言，编程框架为Qiskit



| 量子计算平台                                                 | 量子编程语言/sdk                                             | 文档                                                         | 对接传统语言                             | 备注                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ |
| ![localeI18.QuantumPlatform](README.assets/d2c72bf32e80412eab678d68d2947914.png)[科大国盾](https://quantumcomputer.ac.cn/index.html) | quingo![9086150 quingo 1641482586](README.assets/9086150_quingo_1641482586.png)<br />isq-core | [Quingo (gitee.io)](https://quingo.gitee.io/docs/)<br />[安装和使用 - isQ-core python包使用文档 (arclightquantum.com)](http://www.arclightquantum.com/isq-core/) | quingo: python/C++<br />isq-core: python | 底层指令集为qcis<br />VSCode中有quingo和isq-core的插件支持<br />注意isq和isq-core不同,只有isq-core对接了qcis指令集 |
| ![img](README.assets/credits-imageresMode=sharp2&op_usm=1.5,0.png)[Azure Quantum - 量子云计算服务  Microsoft Azure](https://azure.microsoft.com/zh-cn/products/quantum/) | Q#<br />![Plugins and ecosystem — PennyLane](README.assets/qiskit_logo_small.png)<br />![Cirq - Quantum: Machine Learning & Analytics](https://ml2quantum.com/wp-content/uploads/2020/05/2566b800-6601-11e9-9f2d-36d3354da949.png) | [Q# 程序的运行方式 - Azure Quantum  Microsoft Learn](https://learn.microsoft.com/zh-cn/azure/quantum/user-guide/host-programs?tabs=tabid-python) | python                                   | 可以在visual studio的扩展模块中获得Q#                        |
|                                                              |                                                              |                                                              | python                                   |                                                              |
|                                                              |                                                              |                                                              |                                          |                                                              |

