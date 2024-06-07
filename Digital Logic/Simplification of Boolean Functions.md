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
