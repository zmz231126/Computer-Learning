存储器件的基本模块是一个双稳态（bistable）元件。改元件有两个状态。

<img width="244" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/19711f4a-7f43-41fe-889b-15ea7ea7c427">

上图是由一对连接成环的反相器组成的简单的双稳态元件。

这两个反相器交叉耦合（cross-coupled）。即I1的输入是I2的输出，反之亦然。这个电路没有输入，但是有两个输出。Q 和 Q' 

交叉耦合反相器有两种稳定状态：Q=0 和 Q=1， 所以改电路称为双稳态。 电路可能存在第三种状态，其两个输出均处于0-1之间，
这种状态称为亚稳态（metastable）。

时序电路关注点：
1. 时序电路当前时刻的状态是什么
2. 在输入信号的作用下，下一时刻的状态是什么


## 基本RS锁存器
或非门构成：

<img width="285" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/5a7eec13-aa0c-40e5-bb18-2abd0d0a4da8">

它有两个输入端R S，和两个互补的输出端Q Q‘

$Q (Q_n)$ --> 现态

$Q^{+} (Q_{n+1}$ -->次态

$Q = 0 (Q' = 1)$ -->state 0

$Q = 1 (Q' = 0)$ --> state 1

R 置0端（reset the output to Q=0）

S 置1端（reset the output to Q=1）

<img width="384" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/ac5ad8b2-5d7c-4e55-aa58-da31d6aaa5da">

或非门锁存器对高电平敏感，送入的S R 都是低电平，左右是次态保持

<img width="357" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/d50a5f90-0ee8-4d37-8648-38a03baf162b">

当R 送 1； S 送 0 时， Q=0 表示为0态。所以R 是 置零端。

<img width="326" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/71ac408c-5a19-460e-8f14-ae68591a4ab1">


