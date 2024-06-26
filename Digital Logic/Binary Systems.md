---
title: Binary Systems
Categories:
- 计算机
- Dgital Logic and Computer Design
date: 2025-5-22
tags:
- 数字逻辑

---

# Digit Computers and Digital Systems

Characteristic of a digital system is its manipulation of discrete elements of information. Such as:

- Electric impluses
- The decimal digits
- The letter of an alphabet
- Arithmetric operation
- Punctuation marks
- Any other set of meaningful symbols

> Digit computer —->discrete information processing system

Discrete elements of information  are represented in digital system by physical quantities called **signals**

> Electrical signals such as voltages and current are the most common. 

Discrete quantities of information emerge either from the nature of the process or may be purposely quantized from a continuous process. 

A **analog compute**r performs a simulation of a physical system.

The variables in the analog computer are represented by **continous signals**, usually electric voltage that vary with time.

**Analog computer** has come to mean a computer that manipulates **continuous variables**.

To simulate a physical process in a digital computer, the quantities must be quantized. 

A **physical system** whose behaviour is described by mathematical equations is simulated in a digit computer by means of numerical method.

The **control unit** retrieves intructions, one by one from the program which is stored in **memory**.  For each instruction, the control unit informs the **processor** to execute operation specified in the instruction. Both data and program are stored in memory. The control unit supervises the programm instruction, the processor manipulates the data as specified by the program.

A processor, when combined with the control unit, forms a component referred to as a **central processor unit** or CPU.  

# Binary Numbers

A decimal number such as 7392 can be writen as: 

$7 \times 10^3 + 3 \times 10^2 + 9 \times 10^1 + 2 \times 10^0$

In the context of the this number, 

 "coefficients" refers to the specific numerical values at each position in a decimal number.

"the power of 10" is determined by the position of the coefficient. 

The numerical value of each position is calculated by the coefficient and it's weigh.

The convention is to write only the **coefficients** and from their position deduce the necessary powers of 10. In general, a number with a decimal point is represent by a series of coefficients as follows:

$a_5a_4a_3a_2a_1a_0.a_{-1}a_{-2}a_{-3}$

`a` is one of the ten digits(0,1,2,…9)

subscript value gaves the **place value** and, hence, the power of 10 by which the coefficient must be mutiplied

> The dicimal number system is said to be of **base**, or **radix** 10, because it use ten digits.

---

The **binary** system is a different number system.

-  It's coefficients have two possible values: 0 and 1.
-  It's place value is $2^{subscriptvalue}$.

For example the decimal equivalent of the binary number `11010.11`

$1 \times 2^4 + 1 \times 2^3 + 0 \times 2^2 + 1 \times 2^1 0 \times 2^0 + 1 \times 2^{-1} + 1 \times 2^{-2} = 26.75$

In general, a number expressed in base `r` system has coefficients mutiplied by the power(幂) of `r`.

$a_n \cdot r^n + a_{n-1} \cdot r^{n-1} + \ldots + a_2 \cdot r^2 + a_1 \cdot r^1 + a_0 \cdot r^0 + a_{-1} \cdot r^{-1} + a_{-2} \cdot r^{-2} + \ldots $​   

Two distinguish between number of different bases, we enclose the coefficients in parentheses and wirte a subscript equal to the base. For example:

$(4021.2)_5 = 4 \times 5^3 + 0 \times 5^2 + 2 \times 5^1 + 1 \times 5^0 + 2 \times 5^{-1} = (511.4)_{10}$

```shell
Note: the coefficient values for base 5 can be only be 0,1,2,3,4
```



Arithmetic operations with numbers in base `r` follow the same rules as for decimal number

```markdown
ADDITION:
augend:  101101
addend: +100111
		--------
 sum:	1010100 
		
SUBSTRACTION:  借1得2
minuend:    	101101
subtrahend:	   -100111
			-----------
 difference:	000110
 

Multiplication: 
Multiplicand:	1011
Multiplier:     ×101
				----
				1011
			   0000
			  1011
			  ------
product:	  110111

        101
	---------
1100|110111       
	|1100
	--------
	|000111
	
```

# Number Base Conversions

The conversion from decimal to binary or to any other base `r`system is more convenient if the number  is seperated into an *integer* and a *fraction* part, and the conversion of each part done seperately. 

**Integer**

decimal 41 to binary  (left bottom to right to top)

$\frac{41}{2}$ | $20$ $1$

$\frac{20}{2}$ |$10$  0

$\frac{10}{2}$ |5    0

$\frac{5}{2}$   | 2   1

$\frac{2}{2}$    | 1  0

= 101001

decimal 153 to octal

$\frac{153}{8}$ | 19 1

$\frac{19}{8}$   | 2   3

= 231 

**Fraction**: Multiplication is used instead of division, and integers are accumulated instead of remainders. 

|            | integer | fraction | coefficient(top to down) |
| ---------- | ------- | -------- | ------------------------ |
| 0.6875 * 2 | 1       | 0.3750   | 1                        |
| 0.3750 * 2 | 0       | 0.7500   | 0                        |
| 0.7500 * 2 | 1       | 0.5000   | 1                        |
| 0.5000 * 2 | 1       | 0.000    | 1                        |

(0.6875)<sub>10</sub>= (0.1011)<sub>2</sub>

|           | integer | fraction | coefficient(top to down) |
| --------- | ------- | -------- | ------------------------ |
| 0.513 * 8 | 4       | 0.104    | 4                        |
| 0.104 * 8 | 0       | 0.832    | 0                        |
| 0.832 * 8 | 6       | 0.656    | 6                        |
| 0.656 * 8 | 5       | 0.248    | 5                        |
| 0.248 * 8 | 1       | 0.984    | 1                        |
| 0.984 * 8 | 7       | 0.872    | 7                        |

(0.513)<sub>10</sub>=(0.406517 …)<sub>8</sub>

> The conversion of decimal numbers with both integer and fraction parts is done by converting the integer and fraction seperately and then combining the two answers together. 

(153.0531)<sub>10</sub> = (231.406517)<sub>8</sub>

# Otcal and Hexadecimal Numbers

Since 2<sup>3</sup> = 8 and 2<sup>4</sup> = 16:

- each octal digits corresponds to three binary digits 
- each hexadecimal digits corresponds to four binary digits

Starting from the binary point and proceeding from the left to the right. The corresponding octal digit is then assigned to each group.

$\left(\overbrace{10}^2\overbrace{110}^6\overbrace{001}^1\overbrace{011}^3 \cdot \overbrace{111}^7\overbrace{100}^4\overbrace{000}^0\overbrace{110}^6\right)_2 = (2613.7406)_8$

conversion from binary to hexadecimal is similar, execpt that the binary number is divided groups of four digits:

$\left(\overbrace{10}^2 \overbrace{1100}^C \overbrace{0110}^6 \overbrace{1011}^B \cdot \overbrace{1111}^F \overbrace{0010}^2 \right)_2 = (2C6B.F2)_{16}$

Conversion from octal or hexdecimal to binary is done by a procedure reverse to the above.

$\left(673.124\right)_8 = \underbrace{110}_3\underbrace{111}_7\underbrace{11}_3 \cdot \underbrace{001}_1\underbrace{010}_2\underbrace{100}_4 = (110111.001010100)_2$

> During conmmunication with people, the octal and hexadecimal representation is more desirable because it can express more compactly with a third or a quarter of the number of digits required for the equivalent binary number.

# complements

There are two types of complements for each base `r` system:

**The r's complement**

A positive number N in base r with an integer part of n digits, the r's complement of N is defined as $r^n - N$ and 0 for $N = 0$.

$(52520)_{10 }\Longrightarrow 10^5 - 52520 = 47480$​

> All least significant zero unchanged
>
> The first non-zero least significant digit subtract from 10
>
> All other higher significant digits subtract from 9

$(0.3267)_{10} \Longrightarrow 10^0 - 0.3267 = 0.6733$

$(25.639)_{10}\Longrightarrow 10^2 - 25.639 = 74.361$

$(101100)_2 \Longrightarrow (2^6)_{10} - (101100)_2 = 010100$​

> All least significant zeros unchanged
>
> The first non-zero digit unchanged
>
> All other higher significant digits replace 1 $\to$ 0 and 0 $\to $ 1.

$(4B7)_{16} \Longrightarrow (16^3)_{10} - (4B7)_{16} = (B49)_{16}$​

---

$(72532-3250)_{10}$​

1. Make the two numbers have the same of digit counts, if doesn't equal, add 0 to the left of the shorter one.
2. Add the minuend M to the $r's$ complement of the subtrahend N
3. If and end carry occurs, discard it; If an end carry does not occurs, place a negative sign in frot.

![image-20240525041112081](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202405250411119.png)

![image-20240525041208741](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202405250412793.png)

**The (r-1)'s complement**

A positive number N in base r with an integer part of n digits and a fraction part of m digits, the (r-1)'s complement of N is defined as $r^n - r^{-m} -N$.

$(52520)_{10} \Longrightarrow 10^5 - 10^0 - 52520 = 99999 - 52520 = 47479$​

$(0.3267)_{10} \Longrightarrow 10^0 - 10^{-4} - 0.3267 = 0.9999 - 0.3267 = 0.6732$​

> subtracting every digit from 9

$(101100)_2 \Longrightarrow (2^6)_{10} - (2^0)_{10} - (101100)_2 = 111111 - 101100 = 010011$

> reverse 1 $\to $0 and 0 $\to$ 1

<u>$\text{r's complement }= \text{(r-1)'s complement} + r^{-m}$​</u>

---

$(1010100 - 1000100)_2$

1. make digit count same
2. add minuend M to the $(r-1)'s$ complement of subtrahend N
3. if end carry occurs, add 1 to the least significan digit
4. if end carry does not occurs, place a negative sign in front

> The (r-1)'s complement is used in logical manipulations
>
> The r's complement is used in conjunction with arithmetic application. 



# Binary Codes

There is a direct analogy among binary signals, binary circuit element and binary digits.

Digital systems represent and manipulate not only **binary numbers**, but also many other discrete elements of information.  Any discrete element of information distinct among a group of quantities can be represent by a **binary code**.

>  It is possible to arrange $n$ bits in $2^n$​ distinct ways. 

两位的内存可以存储4组不同的数。4位内存可以存储16个不同的数（$2^4$）

Some bit combinations are unassigned when the number of elements of the group to be coded is not a multiple of the power of 2. For example:

一个三位的内存可以存储的数字有

```shell
1. 000           elements to be coded lets say: 
2. 001
3. 010
4. 011						011
5. 100
6. 101						101
7. 110
8. 111						111
-------------------------------
the remaining 5 combinations are unassigned and not used. 
```



There is minimum number of bits required to code $2^n$ distinct quantities is $n$​, there is no maximum number of bits thtat may be used for a binary code.

**十进制编码**

十进制的每一个数字都需要4位内存。因为8和9的二进制是四位。

- 8421码：8421码又叫BCD码表示，它用二进制形式进行编码，8421指的是权值。比如我们看到计算机的4个位显示为0110，那么用BCD码可以解读为它表示的是十进制的数字6. （$0 \times 8 + 1 \times 4 + 1 \times 2 + 0 \times 1 = 6$）

- 84-2-1码：同样十进制编码的权值可以为负数， 比如84-2-1码。位组合为0110的情况下，代表的就是十进制的2 （$0 \times 8 + 1 \times 4 + 1 \times {-2} + 0 \times {-1} = 2$​）
- Excess - 3 码： T his is an unweighted code, its code assignment is obtained from the corresponding value of BCD after the addition of 3.

Numbers are represented in digital computer either in binary or in decimal through a binary code.

二进制数字和十进制数字在计算机中都是通过二进制编码进行呈现的。

>  **非常有必要清楚：**

>  **把十进制的数字转化为等价的二进制数字（binary numbers）**

> **和把十进制数字进行二进制编码（binary code）的区别**

数码系统中，一连串的0和1可能表示的是二进制数字，也有可能是根据编码规则转换成二进制编码的离散信息。

也有可能两者兼而有之，比如BCD码，当十进制数字是0-9时，它既是二进制数字，而且这个二进制数字又恰好是十进制的数字。但是当大于9时，情况就不同了。比如13， 它的二进制数字时1101，但是BCD编码为00010011.因此。当看到00010011时，就不可以把它当作一个二进制数字看待，它代表的是根据规则变换而来的$(13)_{10}$​. 

For Example, the decimal number 395

The decimal converted to binary is : 110001011

The decimal number in binary code(BCD): 001110010101. occupies four bits for each decimal digit, for a total of 12 bits. The first four bits represent a 3, the next four a 9,  and the last four a 5.

![image-20240528142446974](/Users/ken/Library/Application Support/typora-user-images/image-20240528142446974.png)

The BCD is the most natural to use. The other four-bit codes listed above have one characteristic in common that in not found in BCD. The excess-3, 84-2-1, 2421 are self-complementary codes, that is, the 9's complement of the decimal number is easily obtained by changing 1 to 0. For example:

$(395)_{10} \quad \underrightarrow {2421 code} \quad 0011 1111 1011$ 

It's 9's complement is easily obtained from the replacement of $1\to0, and \quad 0 \to 1$ , Which is 

$(110000000100)_2 \quad \underleftarrow{2421 code} \quad (604)_{10}$

This property is useful when arithmetic operations are internally done with decimal numbers(in a binary code) and subtraction is calculated by means of 9's complement.

**Error Detection Code**

A parity bit is an extra bit included with a message to make the total number of 1 either odd or even. During transfer of information from one location to another, the parity bit is handled as follow:

- In the sending end, the message is applied to a "parity-generation" network where the required parity bit is generated. 
- In the receiving end, all incoming bits are applied to a "parity check" network to check the proper parity adopted. 
- An error in dected if the detected parity  does not correspond to the adopted one. 

The parity method detects the presence of one, third or any odd combination of errors. An even combination of errors is undetectable. 

![image-20240527120606581](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202405271206604.png)

**The Reflected Code**

Digital system can be designed to process data in discrete form only. Data must be converted into digital or discrete form before they are applied to a digital system. Continuous or analog information is converted into digital form by means of an **analog-to-digital converter**. The reflected code is also known as *Gray code*

**Alphanumeric Code**

Alphanumeric code is a binary code of a group of elements consisting of:

-  ten decimal digits
-  the 26 letters of the alphabet
-  a certain number of special symbols such as $

The number of elements in an alphanumeric group is greter than 36. Therefore, it must be coded with a minimum of six bits $2^6 = 64,  2^5 = 32$ is insuufficient.

One possible arrangement is a six-bit alphanumeric code shown in table 1-5 under the name "internal code"

![image-20240528144228282](/Users/ken/Library/Application Support/typora-user-images/image-20240528144228282.png)

 ![image-20240528144246078](/Users/ken/Library/Application Support/typora-user-images/image-20240528144246078.png)

![image-20240528144307182](/Users/ken/Library/Application Support/typora-user-images/image-20240528144307182.png)

Most computer translate the input code into an internal 6-bit code. As an example, the internal representation of name "John Doe" is:

$\overbrace{100001}^J \quad \overbrace{100110}^O \quad \overbrace{011000}^H \quad \overbrace{100101}^N \quad \overbrace{ }^{blank} \quad \overbrace{010100}^D \quad \overbrace{100110}^O \quad \overbrace{010101}^E$

The need to represent more than 64 characters(the lowercase letters and special contrl characters for the transmission of digital information) give rise to seven- and eight bit alphanumeric codes.  One such code is known as ASCII, another code is known as EBCDIC. 

The ASCII listed in Table 1-5 consists of seven bits, but for all practical purposes, an eight-bit code because an eighth bit is invariable added for parity.

<u>Punch Cards 12-bits binary code</u>

# Binary Storage and Registers

The discrete elements of information in a digital computer must have a physical existence in some *information storage medium*.

When discrete elements of information are represented in binary form, *information storage medium* must contain binary storage element for *storing individual bits* 

**Binary cell** is a device that possesses two stable states and is capable for storing one bit of information. 

Example of binary ceel are: flip-flop circuits (触发器电路)

ferrite cores(铁氧体磁芯) used in memories.

**Register ** is a group of binary cells

A register can store one or more discrete elements of information and the same bit configuration may be interpreted differently for different types of elements of information. It is important that the user store meaningful information in registers and that computer be programmed to precess this information according to the **type of information** stored

**register transfer**

The processor unit is composed of various registers that store operands upon which operations are performed. The control unit uses registers to keep track of various computer sequences, and every input and outut device must have at least on register to store the information transferred to or from the device. 

![image-20240528221132665](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202405282211732.png)

 Each time a key is struck, the control enters into the input register an equivalent eight-bit alphanumeric character code

Each eight-bit character transferred to the processor register is preceded by a shift o f the previous character to the next eight cells on its left. When a transfer of four character is completed, the processor register is full, and its contents are transferred into a memory register. 

To precess discrete quantities of information in binary form, computer must be provided with:

1. devices that hold the data to be processed $\rightarrow$ register
2. circuit elements that manipulate individual bits of information $\to$ digital logic circuits

![image-20240528222550438](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202405282225478.png)

# Binary Logic

Binary logic consists of binary variables and logical operations. 

There are three basic logical operations: AND, OR and NOT.

**AND**: $x \cdot y = z $ or $xy =z$ is read "x AND y is equal to z". 

**OR**: $x + y = z$ is read "x OR y is equal to z".

**NOT**: $\bar x = z$ or $x' = z$ is read x not is equal to z

> One should realize that an arithmetic variable designaies a number that may consist of many digits. A logic variable is always either a 1 or 0. 

For example, in binary arithmetic we have 1 + 1 = 10, while in binary logic we have 1+1 = 1

![image-20240529023937773](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406061647641.png)

Electronic digital circuits are sometime called **switching circuits** because they behave like a switch, with the active element such as a transistor either conducting(switch closed) or not conducting(switch open). Instead of changing the switch manually, electrical switching circuits use binary signals to control the conduction or nonconduction state of the active element.

![image-20240529025019896](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406061647288.png)

Electronic digital circuits are also called logic circuits because, with proper input, they establish logical manipulation paths. Any desired information for computing or control can be operated upon by passing binary signals through various combination of logic circuits, each signal representing a variable and carrying one bit of information. 

digital circuits | switching circuits | logic circuits | gates

The NOT gate sometimes called an **inverter** circuit since it inverts a binary signal

![image-20240529025835749](https://raw.githubusercontent.com/zmz231126/bolgpicture/main/202406061647687.png)

Integrated circuits differ from other electronic circuits composed of detachable components. IC cannot be separated or disconnected and the circuit inside the package is accessible only through the external pins.

IC come in two type of packages: flat package and the dual-in-line package

IC are classified in two gereral categories: linear and digital 

1. Linear IC operate with continuous signals to provide electronic functions 
