# the Map Method
- The truth table represention of function is unique, expressed algebraically, if can appera in
many different forms.
- Boolean functions can be simplified by algebraic means. However the prodecure of minimization
  is awkward because it lacks specific rules to predict each succeeding step in the manipulative
  process
- The map method provides a simple straightforward procedure fo minimizing Boolean functions.
  This method may be regarded either as a pictorial form of a truth table or as an extension
  of Venn diagram.

The map represents a visual diagram of all possible ways a function may be expressed in a standard form.
By recognizing various patterns, the user can derive alternative algebraic expressions for the 
same function, from which he can select the simplest one.
> We shall assume that the simplest algebraic expression is any one in a sum of products or product of
> sums that has a minimum number of literals(this expression is not necessarily unique)
对于卡诺图中最小项的排列顺序，就是按照格雷码的顺序排列，然后按照“弓”形填入表格。
它与二进制代码本身内容不相关，只是一种排列方式。但是我们排列好了以后，可以根据真值表确定对应方格的10进制行号。
<img width="736" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/5106661d-ffe0-4000-bf3f-9e43baf15e20">
需要注意的是，卡诺图的来源于用最小项表示的真值表。

我们为什么把真值表中的各个最小项按照反射生成格雷码的方式填入一个个的方格中呢？因为：
1. 最小项真值表中，每两个相邻的最小项只有一个变量不同，每两个相邻的最小项进行逻辑和运算时，销掉不同变量留下相同
   变量$A'B'C' + A'B'C = A'B'(C+C')=A'B'$
2. 通过卡诺图排列以后，我们使这种逻辑相邻转变为了即是逻辑相邻又是几何相邻。
3. 如此我们可以通过观察，直接消除所有相邻项中的不同项，只留下相同项。


for example, $m_5$ and $m_7$ lie in two adjacent squares, Variable y is primed in $m_5$, while the other two are 
the same in both squares. From the postulates of boolean algebra, it follows that the sum of minterms in adjacent 
squares can be simplified into a single $AND$ term consisting only two literals. 
> Any two minterms in adjacent squares thar are $OR$ ed together will cause a remove of the different variable.

For example: $F = x'yz + x'yz' + xy'z' +xy'z$ how to simplified the Boolean function?
1. '1' is marked in each square as needed to represent the function.

   <img width="450" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/0d80b790-2240-4144-bea0-3ca19e2912cb">
   
   this process can be accomplished in two ways:
   - converting each minterm into a binary number, them marking "1" in the corresponding square,
   - by obtaining the coincidence of the variable in each term
3. subdivide the given area area into adjacent squares.在图中显示为两个矩形。
   通过观察每个矩形左方和上方的区域，我们可以得到: $F = x'y + xy'$


然后我们通过观察还发现， $m_0$和 $m_2$ 两个方格的最小值为 $x'y'z'$ 和 $x'yz'$ 它们也只有一个变量不同。它们也是可以消去变化了的变量的
 $x'y'z' + x'yz' = x'z'$
 所以，左右两边的单元格也是属于相邻单元的概念。
 
 比如 $F = x'yz + xy'z' + xyz + xyz'$ 卡诺图表示为：
 
 <img width="468" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/a080c7ea-beaa-408d-8aa3-4a54242c7353">
 
 通过观察卡诺图可以化简为： $F = yz + xz'$

 另外还有一个规律：

 在3变量的卡诺图中，任意4个相邻的方格，都可以直接化简为一个变量。 比如 $F = A'C + A'B + AB'C + BC$ 其卡诺图为：

 <img width="448" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/fd271c44-d9f5-4713-8d74-b41761b95ecf">

 其中剩下的这个变量为四个最小项中的不变项。

 再举一个例子： 
$F(x,y,z) = \sum {0,2,4,5,6}$

这里我们通过10进制的序号给出了最小项，怎么在卡诺图中找到对应的方格呢？这个我们把卡诺图中用二进制数字表示，而不是变量表示。
通过十进制数字对应的2进制数字，找到应该要标记为1的方格的位置。

<img width="414" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/8f7d2487-9715-4aab-a9b0-1a4837ba377c">

通过观察卡诺图直接写出化简后的方程式： $F = z' + xy'$

四变量的卡诺图一样首先在行和列上按照二进制编码的方式排列出变量。the minterm corresponding to each square can be obtained from the
 concatenation of the row number with the column number.

我们用标记为1的方格相加来表示一个函数，那么剩余的方格所所表示的就是这个函数的返函数。

比如我们把卡诺图中标记为0的相邻的方格圈起来，按照同样的方法进行化简，得到的就是这个函数的返函数。

$F(A,B,C,D) = \sum{(0,1,2,5,8,9,10)}$ we mark 0 squre and combined together. We obtained the simplified complemented function 

<img width="462" alt="image" src="https://github.com/zmz231126/Learning/assets/164715631/40d054c8-63b2-46b6-b176-4c95e145668b">

$F' = AB + CD + BD'$

再通过摩根定理(by taking the dual and complementing each literal) 我们就可以得到简化后的和积表达式

$F=(A'+B')(C'+D')(B'+D)$




