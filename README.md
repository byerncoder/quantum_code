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

&emsp;&emsp;谈论量子计算时，我们谈的是n个二态系统(qubit) ，对其执行一系列算符操作，最后执行测量。如下图，我们常常画出横着并排的n条直线，从左到右代表着时间顺序，而不同的直线代表不同的 qubit ；在这些直线上排列着各种小方块大方块还有竖线，代表着各种不同的单 qubit 或多 qubit 幺正算符，每一个幺正算符被称为一个（量子）门；人们常将一些简单的量子门组合成更复杂的量子门；整张图就被称为一个量子网络/量子电路。
![量子电路](/%E9%87%8F%E5%AD%90%E7%94%B5%E8%B7%AF.jpg "量子电路")  
> 一个典型的量子电路  

&emsp;&emsp;人们给一些常用的量子门取了特定的名字，如：

- $\sigma_x$门：  
![$\sigma_x$门](/%E9%9D%9E%E9%97%A8.jpg "$\sigma_x$门")  
X= $\begin{pmatrix} 0&1\\
1&0\\
\end{pmatrix}$   
即在单 qubit 上作用算符$\sigma_x$翻转（简单起见，以后均记做X），相当于经典中的非门。同理，还有Z门和Y\<br>门。

- Hadamard 门：  
![Hadamard 门](/Hadamard%20%E9%97%A8.jpg "Hadamard 门")   
H=$\frac{1}{\sqrt 2} \begin{pmatrix} 1&1\\
1&-1\\
\end{pmatrix}$  
这也是一种单 qubit 门。  

- 控制非(Controlled-NOT, CNOT)门：  
  ![控制非(Controlled-NOT, CNOT)门](/%E6%8E%A7%E5%88%B6%E9%9D%9E(Controlled-NOT%2C%20CNOT)%E9%97%A8.jpg "控制非(Controlled-NOT, CNOT)门")    
  这是一个双 qubit 门，若控制位（图中带黑点的线路）为1，则翻转受控制位（图中带十字圆圈的线路），否则不执行操作；而控制位自身始终不动。

- 控制U\<br>门：
前面我们介绍了控制非门，控制位为1则加$\sigma_x$
到受控位，一个很自然的想法是，能不能推广到如果控制位为1则加任意U
到受控位？  
为了实现这个推广，我们需要如下定理：  
> 设U
为单 qubit 上的任意幺正算符。存在单 qubit 上的幺正算符A,B,C
使得：ABC=I且U=$e^{i\alpha}AXBXC$，其中$\alpha$是某个整体的相因子。

有了这个定理，我们便可以很容易看出，下图所示的电路实现了我们所想要的控制U
门：当控制位为0时，受控位作用ABC=I
相当于没作用；而当控制位为1时，受控位作用AXSXC
，再加上一个整体的相位$e^{i\alpha}$
正好就是U。  
![控制U门](/控制U门.png "控制U门")  

- Toffoli 门：  
对于 CNOT 门另外一个推广的想法是，能不能实现两个门控制一个门？也就是说逻辑与操作能不能做？利用如下这个简单的事实：
> 任意幺正算符是可以开根号的，即对于任意幺正算符U\<br>
，存在幺正算符V\<br>
，使得$V^2=U$。  

具体电路实现见下图:  
![Toffoli 门](/Toffoli%20%E9%97%A8.png "Toffoli 门")  
控制端00输入时，什么门都没有触发，不用管；01输入时，给受控位触发两个门，和效果为零；10输入时，二号控制位翻转，触发$V^+$
，自身再翻转，一号控制位触发V
，和效果为零；11输入时，二号控制位触发V
，翻转两次，一号控制位触发V
，最后总效果为一个U
（在做这些讨论时，始终要记住我们是对一个一般的量子态进行操作，也就是说上面这些情况是可以相干地同时发生的。）。综上，我们实现了预期的功能。当U
取做翻转门X
时，我们一般将其称为 Toffli 门。

### 量子计算的指数加速

#### 量子计算的并行加速和GPU的并行加速的区别

### 量子编程环境



| 量子计算平台                                                 | 量子编程语言/sdk                                             | 文档                                                         | 对接传统语言                             | 备注                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ |
| <img src="README.assets/d2c72bf32e80412eab678d68d2947914.png" alt="localeI18.QuantumPlatform" style="zoom:67%;" />[科大国盾](https://quantumcomputer.ac.cn/index.html) | <img src="README.assets/9086150_quingo_1641482586.png" alt="9086150 quingo 1641482586" style="zoom: 50%;" />quingo<br />isq-core | [Quingo (gitee.io)](https://quingo.gitee.io/docs/)<br />[安装和使用 - isQ-core python包使用文档 (arclightquantum.com)](http://www.arclightquantum.com/isq-core/) | quingo: python/C++<br />isq-core: python | 底层指令集为qcis<br />VSCode中有quingo和isq-core的插件支持<br />注意isq和isq-core不同,只有isq-core对接了qcis指令集<br />quingo同时支持eQASM指令集和QCIS指令集<br />isq-core只支持eQASM<br />该平台目前只开放12比特的量子计算机,支持图形化搭建量子门电路 |
| <img src="README.assets/credits-imageresMode=sharp2&op_usm=1.5,0.png" alt="img" style="zoom: 20%;" />[Azure Quantum - 量子云计算服务  Microsoft Azure](https://azure.microsoft.com/zh-cn/products/quantum/) | Q#<br /><img src="README.assets/qiskit_logo_small.png" alt="Plugins and ecosystem — PennyLane" style="zoom:25%;" /><br /><img src="README.assets/2566b800-6601-11e9-9f2d-36d3354da949.png" alt="Cirq - Quantum: Machine Learning & Analytics" style="zoom: 5%;" /> | [Q# 程序的运行方式 - Azure Quantum  Microsoft Learn](https://learn.microsoft.com/zh-cn/azure/quantum/user-guide/host-programs?tabs=tabid-python)<br />[Qiskit documentation](https://qiskit.org/documentation/)<br />[Cirq Google Quantum AI](https://quantumai.google/cirq) | python                                   |                                                              |
| ![img](README.assets/thid=ODLS.10140edf-ed22-413a-b206-1a1114760d20&w=32&h=32&o=6&pid=13.png)[Quantum Lab - IBM Quantum](https://quantum-computing.ibm.com/lab) | <img src="README.assets/qiskit_logo_small.png" alt="Plugins and ecosystem — PennyLane" style="zoom:25%;" /> | [Qiskit documentation](https://qiskit.org/documentation/)    | python                                   | 进入该平台时不科学上网会报错                                 |
| ![uTools_1681638397635](README.assets/uTools_1681638397635.png)[Google Quantum AI](https://quantumai.google/) | <img src="README.assets/2566b800-6601-11e9-9f2d-36d3354da949.png" alt="Cirq - Quantum: Machine Learning & Analytics" style="zoom:5%;" /><br /><img src="README.assets/OIP.qXYY3inJbVrLSabH3sIjIAHaBIw=379&h=58&c=7&r=0&o=5&dpr=1.1&pid=1.jpeg" alt="OpenFermion 的图像结果" style="zoom:50%;" /><br /><img src="README.assets/tensorflow_quan.jpeg" alt="tensorflow quantum 的图像结果" style="zoom:50%;" /> | [Google Quantum AI](https://quantumai.google/)               | python                                   |                                                              |
|                                                              | <img src="README.assets/torchquantum_logo-300x124.jpeg" alt="TorchQuantum - Quantum ML System" style="zoom:25%;" /> | [TorchQuantum - Quantum ML System (mit.edu)](https://qmlsys.mit.edu/torchquantum/) | python                                   |                                                              |
