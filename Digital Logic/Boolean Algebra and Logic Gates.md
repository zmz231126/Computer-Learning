# Basic Definitions

a set of elements

a set of operators

a number of unproved axioms or postulates

A **binary operator** defined on a set S of elements is a rule that assigns to each pair of elements from S  a unique element from S. For example: 

$ a * b = c$ 

`*` is a binary operator only if :

1. it specifies a rule for finding $c$ from the pair $(a,b)$ 
2. $a,b,c 、\in S$

The most common postulates used to formulate various algebraic structures are:

1. **Closure**（封闭性）: 

   We say a set S is closed with respect to a binary operator if: for <u>every</u> pair of elements of S, the bianry operator specifies a rule for obtaining a unique element of S.

   We say a set S is not closed with respect to a binary operator if : the obtained unique operator is not from S.

   natural Number $N = {\{1,2,3,4, \ldots\}}$  N is closed with respect to the binary operator plus $+$ , while  N is not closed with respect to the binary operator minus $-$​.

   一个集合对某个运算符来说具有封闭性。在某一个二元运算符下，一个集合能否“自给自足”，不会产生超出自身范围的元素。

2. **Associatiove law**（结合律）: a binary operator is said to be associative whenever:

   $(x*y)*z = x*(y*z)$  for all $x,y,z \in S$  

3. **commutative law**(交换律)：a binary operator * on a set S is said to commutative whenever:

   $x*y = y*x$ for all $x,y \in S$

4. **Identity element**:(单位元)

   A set $S$ is said to have an identity element with respect to a binary operator $*$ if there exists an element $e \in S$ with the property:

   $e *x = x*e = x$ for every $x \in S$

   the element 0 is identity element with respect to binary operator + on the set of integers $I$ since: $ x + 0 = 0+ x = x \quad \text{for any} \quad x \in I$​

   The set of natural number $N$ has no identity number since 0 is excluded from the set.

5. **Inverse**(逆元)： 

   A set $S$ having the identity element $e$ with respect to a binary operator  is said to have an inverse whenever, for every $x \in S$, there exists a element $y \in S$ such that:

   $x *y = e$  for example:

   In the set of integers $I$ with identity element $e = 0$, the inverse of an element $a$ is $(-a)$ since $a + (-a) = 0$

6. **Distributive law**:(分配律)：

   If $*$ and $\cdot$ are two binary operators on a set $S$, $\ast$ is said to distributive over $\cdot$ whenever:

   $x \ast (y\cdot z)=(x*z)\cdot(y*z)$​

不同的运算符对应各种不同的规律。比如逆元，运算符不同对应的逆元也不一样。

# Axiomatic Definiton of Boolean Algebra

Boolean Algebra is an algebric structure defined on a set of element $B$ together with two binary operator $ + \text{ and} \cdot$​ provided the following postulates are satisfied.



1. Closure with respect to the operator $+$ and operator $\cdot$​ 

2. $+$ 运算符下，单位元是0； $\cdot$​​ 运算符下，单位元是1 

   $x + 0 = 0 + x = x$

   $x \cdot 1 = 1 \cdot x = x $

3. 两个运算符满足交换律

4. 两个运算符都同时满足交换律，比如：

​	$x \cdot (y + z) = (x\cdot y) + (x \cdot z)$ 

​	$x + (y \cdot z) = (x+y)\cdot (x+z)$

5. $+$ 运算符下，反元是1；$\cdot $​ 运算符下，反元是0

​	$ x + x' = 1$

​	$x \cdot x' = 0$

6. There exist at least two elements $x,y \in B$ such that $ x \ne y$



Boolean Algebra resembles ordinary algebra in some respects, but beginner must be careful not to substitute the rules of ordianry algebra where they are not applicable.

One party can be obtained from the other if the binary operators and the identity element sare interchanged.

逻辑代数里边的几个公理和定理应该记下来：

**operator precedence**
parentheses > NOT > AND > OR

**Venn Diagram**
相加表示两部分组合一起，相乘表示两部分重叠

![image-20240602013928102](/Users/ken/Library/Application Support/typora-user-images/image-20240602013928102.png)

Veen Diagram may be used to illustrate the postulates of Boolean algebra or to show the validity of theorems.

![image-20240602014328952](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406020143973.png)

the area belonging to xy is inside the circle x therefore $x = xy +x $

![image-20240602014517847](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406020145870.png)

# Boolean Function

a boolean function is an expression formed with:

- binary variables
- binary operators OR, AND, NOT,  parentheses, 
- equal sign

Any boolean function can be represented in a truth table. The number of rows in the table is $2^n$, where n is the number of binary variables in the function. For each row of the table, there is a value for the function equal to either 1 or 0. 

In general, two functions of n bianry variables are said to be equal if they have the same value for all possible $2^n$ combination of the $n$ variables

![image-20240602020443383](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406020205669.png)

for example $F_3 = F_4$ . The manipulation of Boolean algebra is applied mostly to the problem of finding simpler expression for the same function.

A boolean algebra may be transformed from an algebraic expression into a logic diagram composed AND, OR, and NOT gates.

![image-20240602020953821](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406020209844.png)

In digital logic, a Boolean function is a mathematical representation of a logic circuit, and it can be implemented using logic gates such as AND, OR, NOT, NAND, NOR, XOR, and XNOR. Each literal in a Boolean function corresponds to an input to a gate or a combination of gates, and each term (which can be a single literal or a combination of literals connected by AND/OR operations) is implemented using one or more logic gates. Here's a breakdown of how this works:

- **Literals**: In a Boolean function, a literal is a basic variable or its negation. For example, in the function $f(A, B) = A + \overline{B}, (A) \quad and \quad\overline{B}$ are literals. Each literal represents an input to the circuit, which can be directly from an input pin or the output of another gate. In this example, \($A$\) would be a direct input, and \($\overline{B}$\) would be implemented using a NOT gate on input \(B\).

- **Terms**: A term is a product (AND operation) of literals or a sum (OR operation) of products. Each term in a Boolean function can be implemented using AND gates for products and OR gates for sums. For instance, in the function $f(A, B, C) = AB + \overline{A}C$, \($AB$\) and \($\overline{A}C$\) are terms. The term \(AB\) would be implemented using an AND gate with inputs \(A\) and \(B\), and \($\overline{A}C$\) would be implemented using an AND gate with inputs from a NOT gate (for \($\overline{A}$\)) and \(C\).

- **Complex Functions**: More complex functions might require a combination of several gates to implement each term and additional gates to combine these terms according to the function's logic. For example, a function like \(f(A, B, C) = (A + B)\overline{C}\) would require an OR gate for \(A + B\), a NOT gate for \(\overline{C}\), and an AND gate to combine the two results.

The implementation of Boolean functions with logic gates is a foundational concept in digital electronics, enabling the design and construction of digital circuits that perform specific logical operations. This principle is applied in designing everything from simple logic circuits to complex digital systems like microprocessors and memory units.

**Duality**

If the dual of an algebraic expression is desired, we simply interchange OR and AND operators and replace 1 to 0, 0 to 1.

对偶原理：如果一个逻辑表达式为真，那么我们交换AND和OR运算符，并且将0和1互换，得到的新表达式依然为真比如：

$x+xy = x$ 那么$x(x +y) = x$

**Complement of a Function**

follows the rule of dual 

$F_1 = x'yz' + x'y'z$​

$F_1' = (x + y' + z)(x + y + z')$

根据摩根定理反函数也是将AND 和 OR对换， 每一个因子取反。

**Minterm**

A bianry variable may appear either in its normal form(x) or in its complement form(x'). 

- 现在有两个二元变量。

- 二元运算符为AND。

那么他们可能出现的组合形式为$x'y',x'y,xy',xy$.

这四种结果就叫做minterm或者standard product.

如果有$n$个二元变量，那么就会有$2^n$个minterm.

每一个变量，如果对应“位”的二进制数字是$0$，那么我们就给变量加上"$'$"。

如果变量对应"位"的二进制数字是$1$，那么我们就将这个变量不标记"$’$"。

每一个minterm我们给它做一个代号$m_j$。其中$j$表示的是从$0\to 2^{n-1}$的十进制计数。

![image-20240603024417026](/Users/ken/Library/Application Support/typora-user-images/image-20240603024417026.png)

**Maxterm**

相对应的，如果我们将AND更换位OR, 那么我们就得到了maxterm.不同的是，我们这里如果变量对应的$0$，我们就给变量加"$'$"，如果变量对应的是$1$，我们就给变量加"$'$"。

> 需要注意到的是，maxterm是它对应的minterm的补码。

![image-20240603025012879](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406032050541.png)

任何一个布尔函数都可以根据真值表，用最小项函数的形式表示出来。比如有一个布尔函数$f_1$，3个变量。当三个变量为001,100,111时，$f_1$都等于1.此时，我们就可以用最小项函数表示这个布尔函数为:

$f_1 = x'y'z + xy'z'+ xyz=m_1 + m_4 +m_7$ 也就是说函数$f_1$在$m_1,m_4,m_7$的任意一个组合下都是1。那么我们就可以推理出，$f_1$在$m_1,m_4,m_7$之外的所有组合情况都是0。所以$f_1= M_0\cdot M_2 \cdot M_3 \cdot M_5 \cdot M_6$

同样的根据表2-4我们也可以看出来当三个变量为011，101，110，111时，函数$f_2 =1$。我们用最小项函数可以表示为$f_2 = x'yz + xy'z + xyz'+ x'y'z'= m_3 + m_5+m_6+m_7$

通过以上两个例子可以看出来，任何一个布尔函数都可以用最小项函数的形式表示出来 **a sum of minterms**也可以用最大项函数表示出来**product of maxterm**，这两种形式叫做规范形式 **canonical form**

$F = A + B'C$​​ 这里我们最长用到的时$x + x' = 1$

$= A (BC + (BC)') + B'C(A+A')$

$= ABC + A(B'+C') + AB'C + A'B'C$

$= ABC + AB' + AC' + AB'C +A'B'C$​

$= ABC + AB'C + AB'C' + ABC' + AB'C' + AB'C + A'B'C$​

$=ABC + AB'C + AB'C' + ABC' + A'B'C$​

Rearranging the minterms in ascending order, we finally obtain:

$F = m_1 + m_4 +m_5+m_6+m_7$

More oftern we write:

$F(A,B,C)=\sum(1,4,5,6,7)$​

$F = xy + x'z$ 这里我们最长用到的是分配律。和$x \cdot x'=0$​

$= (xy +x')(xy + z)$

$=(x+x')(x'+y)(x+z)(y+z)$

$= (x'+y)(x+z)(y+z)$​

$= (x'+y+z \cdot z')(x+z+ y \cdot y')(x \cdot x' +y +z)$

$=(x'+y +z)(x'+y+z')(x+z+y)(x+z+y')(y+z+x)(y+z+x')$

$= (x'+y+z)(x'+y+z')(x+y+z)(x+y'+z)$

$= M_0M_2M_4M_5$

$F(x,y,z)= \prod(0,2,4,5)$

# Digital Logical Gates

![image-20240605003214367](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050032431.png)

The inverter circuit inverts the logic sense of a binary variable. It produce the NOT, or complement, function. The small symbol in the output of the graphic symbol of an inverter designates the logic complement. The triangle by itself designates a buffer circuit. 

The buffer produces the transfer function but does not produce any particular logic operation.

The **NAND** and **NOR** gates are extensively used as standard logic gates and in fact far more popular than the AND and OR gates. 

比如可以用一个NOR门构建一个AND门

![image-20240605024134665](/Users/ken/Library/Application Support/typora-user-images/image-20240605024134665.png)

The **Exclusive-OR**(异或) 相同得0，不同得1， has a graphic symbol similar to the OR gate, except for the additional curved line on the input side. 

The **Exclusive-NOR** or **Equivalence** is the complement of the **exclusive_OR**相同得1，不同得0.

> NAND and NOR 并不适用结合律。

![image-20240605022229239](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050222319.png)

$x \downarrow(y \downarrow z) \ne (x \downarrow y) \downarrow z$

$x \downarrow (y \downarrow z) = [x + (y + z)']' = x'(y+z)= x'y + x'z$

$(x \downarrow y) \downarrow z = [(x+y)' + z]' = (x+y)z' = xz' + yz'$

跟两输入端的规则一样，多输入端下$NAND $和$NOR$ 的规则为:

$x \downarrow y \downarrow z = (x + y + z)'$​

![image-20240605022337614](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050223701.png)

$x \uparrow y \uparrow z = (xyz)'$​

![image-20240605022350973](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050223023.png)

在书写嵌套式$NAND$ 或者$NOR$运算时，需要注意用括号来指明运算顺序

![image-20240605022440181](/Users/ken/Library/Application Support/typora-user-images/image-20240605022440181.png)

$F = [(ABC)' \cdot (DE)']' = ABC + DE$

> Exclusive-OR 和Equivalence gates 适用于交换律和结合律。

多输入端口下，一般不会使用这两种门，两输入端口也多用其他门表示。

- The exclusive-gate是一个 odd function. 只有当输入端有奇数个1时，才会输出1
- The equivalence function is an even function. 只有当输入端有偶数个0时，才会输出1.

![image-20240605023922206](/Users/ken/Library/Application Support/typora-user-images/image-20240605023922206.png)

# IC Digital Logic Families

The basic circuit in each family is either a $NAND$ or $NOR$ gate.  The electronic components employed in the construction of basic circuit are usually used to name the logic family.

**TTL**TTL代表晶体管-晶体管逻辑（Transistor-Transistor Logic），是一种数字集成电路技术。TTL电路使用双极型晶体管（BJT）作为开关元件，常用于数字电子系统中。<u>最流行</u>

**ECL**代表发射极耦合逻辑（Emitter-Coupled Logic），是一种高速数字集成电路技术。ECL电路使用双极型晶体管（BJT）作为基本的开关元件，具有非常快的响应速度和高的工作频率。ECL电路通常用于高性能的数字系统中，如超大规模集成（VLSI）电路和通信系统中的高速电路。<u>高速度</u>

**MOS**代表金属-氧化物-半导体（Metal-Oxide-Semiconductor），是一种常见的半导体器件结构。MOS结构由金属电极、氧化物绝缘层和半导体材料组成。<u>高集成度</u>

**CMOS**代表互补金属氧化物半导体（Complementary Metal-Oxide-Semiconductor）<u>低功耗</u>

$I^2L$代表综合注入逻辑（Integrated Injection Logic）<u>高集成度</u>

LSI通常指大规模集成电路，MSI是中等规模集成电路，而SSI是小规模集成电路。不同的集成电路家族在不同规模的集成电路中有着各自的优势和应用领域。

**TTL gates**

A 14-pin package can accommodate only four two-input gate

each gate requires 3 external pins, two each for inputs and one each for output, for a total of 12 pins.

the remaining two pins are needed for supplying power to the circuits.

![image-20240605030604327](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050306377.png)

The terminals marked $V_{cc}$ and $GND$ are the power supply pins which require a voltage of 5 volts for proper operation.

**ECL Gates**

![image-20240605031751314](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406050317359.png)

Note that an ECL gate may have two outputs. One for the NOR function, and another for the OR function (pin 9 of the 10102IC)

ECL gate have three terminals for power supply. $V_{cc1} $and $V_{cc2}$ are usually connected to ground, and $V_{EE}$ to a 5.2 volt supply.

**CMOS**

![image-20240605032500252](/Users/ken/Library/Application Support/typora-user-images/image-20240605032500252.png)

每个电路都有两个未使用的端口marked as NC(no connection). the terminal $V_{ss}$ is connected to ground, $V_{DD}$ requires a power supply voltage from 3~15 volts.

# Positive and Negative Logic

Two signal values are assigned to two logic values, there exist two different assignments of signals to logic. 

- positive-logic system: Choosing the high-level $H$ to represent logic-1
- negative-logic system: Choosing the low-level $L$ to represent logic-1

Intergrated-circuit data sheets define digital functions not in terms of logic-1, logic-0, but rather in terms of $H$ and $L$ levels. It's up to the user to decide on a positive or negatic logic assignment..



Because of the principle of duality of Boolean algebra, an interhcange of signal-value assigment results in a dual-function implementation.

![image-20240606013708818](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406060137876.png)

This physical gate can function as either a $NAND$ or $NOR$ gate, depending on the polarity assignment.

In any case, if negative logic is assumed in any input or output terminal, it is necessary to include the polarity indicator triangle symbol along the terminal. 

![image-20240606014617737](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406060146790.png)

# special characteristics

**Fan-out**: the number of standard loads that the output of gate can drive without impairing its operation. 

A standard load is usually defined as the amount of current needed by an input of another gate in the same IC family. 

The output of a gate can supply a limited amount of current. 

非反相放大器（Noninverting amplifiers）或缓冲器（buffers）有时被用来为重负载提供额外的驱动能力。

- 非反相放大器：非反相放大器是一种放大器电路，其输出信号与输入信号同相（即不发生相位反转）。它通常用于增加信号的幅度而不改变其相位。
- 缓冲器：缓冲器是一种电路，用于增强信号的驱动能力，使其能够推动重负载而不降低信号质量。缓冲器通常用于防止信号衰减或失真，特别是在需要长距离传输信号或连接到多个输入时。通过使用非反相放大器或缓冲器，可以增强电路的驱动能力，确保信号传输的可靠性和稳定性。

**Power dissipation**: is the supplied power required to operate the gate. In a given system, there may be may ICs, and the power required by each IC must be considered. ($mW$)

**Propagation delay**: is the average transition delay time for a signal to propagate from input to oupt when the binary signals change in value. $1ns = 10^{-9}sec$

**Noise margin** is the maximum noise voltage added to the input signal of a digital circuit that does not cause an undesirable change in the circuit output.

