# quantum_code

## 论文来源和作者详情信息

### 论文来源

&emsp;&emsp;本篇论文来自2015年10月的《物理评论快报》（Physical Review Letters）。  
&emsp;&emsp;1958年为了快速发表重要的物理研究成果，美国《物理评论》主编塞缪尔•古兹密特（Sam Goudsmit）做出一个决定：将《物理评论》中的一个栏目——《给编辑的快报》——分离出来，办一份新期刊，刊名就是《物理评论快报》（Physical Review Letters）。1958年7月1日，第一期含有25篇论文的PRL正式出版，这也是世界物理学界第一份快报类期刊。到现在，它已经成为国际物理学界最权威的期刊之一。  
&emsp;&emsp;PRL很注重文章的原创性，一些重要但是原创性不高的文章会以观点不新颖拒稿之后推荐到PR系列期刊上。而且PRL讲究理论跟实验的结合，缺一边都容易给审稿人揪住辫子不放，所以导致现在审稿越来越严，命中越来越难。按照现在网站的说法，录用率在20%的样子。实际上，在2009年前，录用率还是30%的样子的。2009年的时候，PRL决定限制文章数量，只发表那些很重要的文章。在大部分期刊选择扩张的时候，PRL反其道而行，更加严格的筛选文章的质量，让人觉得更加值得敬佩，也进一步巩固了期刊的声誉。  
&emsp;&emsp;《物理评论快报》为中科院1区期刊，JCR分区为Q1，2022年的影响因子为9.185,且PRL在Physics and Astronomy 领域的H-index远高于其他杂志，处于统治地位。PRL是物理领域的标尺，发PRL是每个物理人的梦想。    
![物理评论快报](README.assets/prl.jpg "物理评论快报")


### 作者详情
&emsp;&emsp;本文由中国科学技术大学合肥微尺度物理科学国家实验室和近代物理系和中国科学技术大学量子信息与量子物理协同创新中心的李兆凯,刘晓梅,徐南阳,杜江峰所写。  

- 李兆凯  
  中国科学技术大学副研究员。从事基于自旋共振的量子计算与量子模拟的实验研究工作多年，在磁共振量子操控上有着丰富的实验经验，取得了量子人工智能算法实现手写识别、压缩量子模拟、量子化学基态问题、线性方程组求解等一系列重要的科学研究成果，相继发表于国际知名SCI期刊 Nature Physics (1篇)、Science Advances（1篇）、Physics Review Letters（6篇)等杂志上。目前主要研究方向为机器学习与量子计算的交叉，探索实用新型量子算法，在自旋量子计算体系上运行量子机器学习算法，展现出其解决人工智能问题的能力。

- 杜江峰  
  中国科学院院士，中国科学技术大学教授， 教育部长江学者特聘教授，国家杰出青年科学基金获得者，国家重大科学研究计划项目首席科学家，首批国家万人计划“中青年科技创新领军人才”入选者，新世纪百千万人才工程国家级人选。长期从事量子物理及其应用的实验研究，是国际上自旋量子计算和模拟、量子精密测量实验研究方面有突出贡献的学者之一，在包括 Science (3篇)、Nature (2 篇)、Nature 子刊(13 篇)、Phys. Rev. Lett. (34 篇)在内的国际学术期刊上发表论文 200余篇，SCI 他引 5200 余次。

- 徐南阳  
黄山青年学者”教授，理学博士，2012年毕业于中国科学技术大学，博士毕业后留任中国科学技术大学物理学院特任副教授。主要研究方向为基于电子自旋的控制和探测技术，量子计算机体系架构，量子算法等。曾在国际顶级物理学杂志Phys.Rev.Lett.（物理评论快报）上发表7篇研究论文（其中三篇为第一或通讯作者），涵盖绝热量子算法，量子模拟，量子人工智能等方面。

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
![量子电路](README.assets/%E9%87%8F%E5%AD%90%E7%94%B5%E8%B7%AF.jpg "量子电路")  
> 一个典型的量子电路  

&emsp;&emsp;人们给一些常用的量子门取了特定的名字，如：

- $\sigma_x$门：  
![$\sigma_x$门](README.assets/%E9%9D%9E%E9%97%A8.jpg "$\sigma_x$门")  
X= $\begin{pmatrix} 0&1\\
1&0\\
\end{pmatrix}$   
即在单 qubit 上作用算符$\sigma_x$翻转（简单起见，以后均记做X），相当于经典中的非门。同理，还有Z门和Y\<br>门。

- Hadamard 门：  
![Hadamard 门](README.assets/Hadamard%20%E9%97%A8.jpg "Hadamard 门")   
H=$\frac{1}{\sqrt 2} \begin{pmatrix} 1&1\\
1&-1\\
\end{pmatrix}$  
这也是一种单 qubit 门。  

- 控制非(Controlled-NOT, CNOT)门：  
  ![控制非(Controlled-NOT, CNOT)门](README.assets/%E6%8E%A7%E5%88%B6%E9%9D%9E(Controlled-NOT%2C%20CNOT)%E9%97%A8.jpg "控制非(Controlled-NOT, CNOT)门")    
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
![控制U门](README.assets/控制U门.png "控制U门")  

- Toffoli 门：  
对于 CNOT 门另外一个推广的想法是，能不能实现两个门控制一个门？也就是说逻辑与操作能不能做？利用如下这个简单的事实：
> 任意幺正算符是可以开根号的，即对于任意幺正算符U\<br>
，存在幺正算符V\<br>
，使得$V^2=U$。  

具体电路实现见下图:  
![Toffoli 门](README.assets/Toffoli%20%E9%97%A8.png "Toffoli 门")  
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
