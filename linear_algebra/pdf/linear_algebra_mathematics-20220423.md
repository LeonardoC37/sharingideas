### Linear Algebra 

1. 设$A$是$m{\times}n$矩阵，$B$是$n{\times}s$矩阵，若$AB=O$，证明$rank(A)+rank(B){\leq}n$.

   [解答]

   分析：总体思路：采用矩阵分块的方式求解.题目具有一定难度.

   证明：
   对矩阵$B$按照列分块，我们记$B$ = $\begin{bmatrix}{\beta}_1&{\beta}_2&{\beta}_3&{\cdots}& {\beta}_s\\
   \end{bmatrix}\\$
   那么有
   $$
   \begin{aligned}
   AB&=A\begin{bmatrix}
   {\beta}_1&{\beta}_2&{\beta}_3&{\cdots}& {\beta}_s\\
   \end{bmatrix} \\ &= \begin{bmatrix}
   A{\beta}_1&A{\beta}_2&A{\beta}_3&{\cdots}& A{\beta}_s\\
   \end{bmatrix} \\
    & = \begin{bmatrix}
   \vec{0}&\vec{0}&\vec{0}&{\cdots}& \vec{0}\\
   \end{bmatrix}
   \end{aligned}
   $$
   于是我们有$A{\beta}_j = \vec{0},j = 1,2,3,{\cdots},s$,
   所以$B$的列向量都是齐次方程组$A\vec{x} = \vec{0}$的解，由于方程组$A{\vec{x}} = \vec{0}$的解向量的$rank(\vec{x}) = n - rank(A)$,这里的$\vec{x}$与$\vec{\beta}$含义等价，所以
   $$
   rank( {\beta}_1,{\beta}_2,{\beta}_3,{\cdots}, {\beta}_s){\leq}n-rank(A)
   $$
   我们又知道
   $$
   rank( {\beta}_1,{\beta}_2,{\beta}_3,{\cdots}, {\beta}_s) = rank(B)
   $$
   所以：$rank(A)+rank(B){\leq}n$.

2. 设有实矩阵 $A=\left[\begin{array}{ccc}1 & 2 & 3 \\ 2 & 3 & 5 \\ 1 & 1 & a\end{array}\right] ， B=\left[\begin{array}{ccc}1 & b & c \\ 2 & b^{2} & c+1\end{array}\right]$ ，其中 $a, b, c$ 为实常数. 已知齐次线性方程组 $A X=0$ 和 $B X=0$ 同解，试求 $a, b, c$ 的值. 

   [解答]

   解:由题意，矩阵 $A$ 和 $B$ 必然有相同的秩，从而 $A$ 必然不满秩，于是
   $$
   \operatorname{det} A=\operatorname{det}\left[\begin{array}{lll}
   1 & 2 & 3 \\
   1 & 1 & 2 \\
   1 & 1 & a
   \end{array}\right]=0
   $$
   得 $a=2$.
   设 $X=\left(x_{1}, x_{2}, x_{3}\right)^{T}$ ，解方程组 $A X=0$ 得 $X=t(1,1,-1)^{T}$ ，其中 $t$ 为任意实数. 这也说明两个方程组的解空间维数都是 1 ，从而矩阵 $A$ 和 $B$ 的秩都是 2 .
   令 $B\left[\begin{array}{c}1 \\ 1 \\ -1\end{array}\right]=0$ ，得 $\left\{\begin{array}{l}b-c+1=0 \\ b^{2}-c+1=0\end{array}\right.$ ，解得 $\left\{\begin{array}{l}b=0 \\ c=1\end{array}\right.$ 或 $\left\{\begin{array}{l}b=1 \\ c=2\end{array}\right.$.
   进一步计算可得，当 $b=0, c=1$ 时， $B$ 的两行线性相关，此时 $B$ 的秩为 1 ；而当 $b=1, c=2$ 时， $B$ 的两行线性无关，此时 $B$ 的秩为 2 .
   综上所述， $a=2, b=1, c=2$.

3. 证明替换定理：设向量组 $\left\{\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \ldots, \boldsymbol{\alpha}_{s}\right\}$ 线性无关，$\boldsymbol{\beta}=b_{1} \boldsymbol{\alpha}_{1}+b_{2} \boldsymbol{\alpha}_{2}+\cdots+b_{s} \boldsymbol{\alpha}_{s}$. 如果 $b_{i} \neq 0$ ，那么用 $\boldsymbol{\beta}$ 替换 $\boldsymbol{\boldsymbol { \alpha } _ { i }}$ 后得到的向量组 $\left\{\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \ldots, \boldsymbol{\alpha}_{i-1}, \boldsymbol{\beta}, \boldsymbol{\alpha}_{i+1}, \ldots, \boldsymbol{\alpha}_{s}\right\}$ 也线性无关.
   [解答]

   证明：设存在标量 $c_{1}, c_{2}, \ldots, c_{s}$ 使得
   $$
   c_{1} \boldsymbol{\alpha}_{1}+c_{2} \boldsymbol{\alpha}_{2}+\cdots+c_{i-1} \boldsymbol{\alpha}_{i-1}+c_{i} \boldsymbol{\beta}+c_{i+1} \boldsymbol{\alpha}_{i+1}+\cdots+c_{s} \boldsymbol{\alpha}_{s}=0
   $$
   即
   $$
   \left(c_{i} b_{1}+c_{1}\right) \boldsymbol{\alpha}_{1}+\left(c_{i} b_{2}+c_{2}\right) \boldsymbol{\alpha}_{2}+\cdots+\left(c_{i} b_{i-1}+c_{i-1}\right) \boldsymbol{\alpha}_{i-1}+b_{i} \boldsymbol{\alpha}_{i}+\left(c_{i} b_{i+1}+c_{i+1}\right) \boldsymbol{\alpha}_{i+1}+\cdots+\left(c_{i} b_{s}+c_{s}\right) \boldsymbol{\alpha}_{s}=0
   $$
   因为向量组 $\left\{\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \ldots, \boldsymbol{\alpha}_{s}\right\}$ 线性无关，所以
   $$
   c_{i} b_{1}+c_{1}=c_{i} b_{2}+c_{2}=\cdots=c_{i} b_{i-1}+c_{i-1}=b_{i} c_{i}=c_{i} b_{i+1}+c_{i+1}=\cdots=c_{i} b_{s}+c_{s}=0
   $$
   因为 $b_{i} \neq 0$ ，所以 $c_{i}=0$ ，所以 $c_{1}=c_{2}=\cdots=c_{n}=0$.
   这说明向量组 $\left\{\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \ldots, \boldsymbol{\alpha}_{i-1}, \boldsymbol{\beta}, \boldsymbol{\alpha}_{i+1}, \ldots, \boldsymbol{\alpha}_{s}\right\}$ 是线性无关的.

4. 范德蒙行列式形式： $D=\left[\begin{array}{ccccc}1 & 1 & 1 & \ldots & 1 \\ x_{1} & x_{2} & x_{3} & \ldots & x_{n} \\ x_{1}^{2} & x_{2}^{2} & x_{3}^{2} & \ldots & x_{n}^{2} \\ \ldots & \ldots & \ldots & \ldots & \ldots \\ x_{1}^{n-2} & x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-2} \\ x_{1}^{n-1} & x_{2}^{n-1} & \ldots & \ldots & x_{n}^{n-1}\end{array}\right]$
   遇到类似于上式的行列式时，可以使用范德蒙行列式直接计算此行列式的值。具有上式特征的行列式的值为: $\prod\limits_{n \geq i>j \geq 1}=\left(x_{i}-x_{j}\right)$
   上式表示: 行列式 $D$ 的值为所有的 $\left(x_{i}-x_{j}\right)$ 的乘积 (其中 $\mathrm{i}>\mathrm{j}$ ).

   [证明]

   通过观察范德蒙行列式，拿行列式的第一列来说，相邻的两个元素，上面的元素比下面的元素少乘 一次 $x_{1}$ 。根据这一特征，可以试着从第 $\mathrm{n}$ 行开始，每个元素都减去前一行元素的 $x_{1}$ 倍，行列式就变为:
   $$
   \begin{aligned}
   &D=\left[\begin{array}{ccccc}
   1 & 1 & 1 & \ldots & 1 \\
   x_{1} & x_{2} & x_{3} & \ldots & x_{n} \\
   x_{1}^{2} & x_{2}^{2} & x_{3}^{2} & \ldots & x_{n}^{2} \\
   \ldots & \ldots & \ldots & \ldots & \ldots \\
   x_{1}^{n-2} & x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-2} \\
   x_{1}^{n-1} & x_{2}^{n-1} & \ldots & \ldots & x_{n}^{n-1}
   \end{array}\right]=\left[\begin{array}{cccccc}
   1 & 1 & \ldots & 1 \\
   x_{1}-x_{1} & x_{2}-x_{1} & x_{3}-x_{1} & \cdots & x_{n}-x_{1} \\
   x_{1}^{2}-x_{1} \cdot x_{1} & x_{2}^{2}-x_{1} \cdot x_{2} & x_{3}^{2}-x_{1} \cdot x_{3} & \ldots & x_{n}^{2}-x_{1} \cdot x_{n} \\
   \ldots & \ldots & \ldots & \ldots & \ldots \\
   x_{1}^{n-2}-x_{1} \cdot x_{1}^{n-3} & x_{2}^{n-2}-x_{1} \cdot x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\
   x_{1}^{n-1}-x_{1} \cdot x_{1}^{n-2} & x_{2}^{n-1}-x_{1} \cdot x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}
   \end{array}\right]\\
   &=\left[\begin{array}{ccccc}
   1 & 1 & 1 & \ldots & 1 \\
   x_{1}-x_{1} & x_{2}-x_{1} & x_{3}-x_{1} & \ldots & x_{n}-x_{1} \\
   x_{1}^{2}-x_{1}^{2} & x_{2}^{2}-x_{1} \cdot x_{2} & x_{3}^{2}-x_{1} \cdot x_{3} & \ldots & x_{n}^{2}-x_{1} \cdot x_{n} \\
   \ldots & \ldots & \ldots & \ldots & \ldots \\
   x_{1}^{n-2}-x_{1}^{n-2} & x_{2}^{n-2}-x_{1} \cdot x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\
   x_{1}^{n-1}-x_{1}^{n-1} & x_{2}^{n-1}-x_{1} \cdot x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}
   \end{array}\right] \\
   &=\left[\begin{array}{ccccc}1 & 1 & 1 & \ldots & 1 \\ 0 & x_{2}-x_{1} & x_{3}-x_{1} & \ldots & x_{n}-x_{1} \\ 0 & x_{2}^{2}-x_{1} \cdot x_{2} & x_{3}^{2}-x_{1} \cdot x_{3} & \ldots & x_{n}^{2}-x_{1} \cdot x_{n} \\ \ldots & \ldots & \ldots & \ldots & \ldots \\ 0 & x_{2}^{n-2}-x_{1} \cdot x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\ 0 & x_{2}^{n-1}-x_{1} \cdot x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}\end{array}\right] \\
   &  =1 \times\left[\begin{array}{cccc}x_{2}-x_{1} & x_{3}-x_{1} & \ldots & x_{n}-x_{1} \\ x_{2}^{2}-x_{1} \cdot x_{2} & x_{3}^{2}-x_{1} \cdot x_{3} & \cdots & x_{n}^{2}-x_{1} \cdot x_{n} \\ \ldots & \ldots & \ldots & \cdots \\ x_{2}^{n-2}-x_{1} \cdot x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\ x_{2}^{n-1}-x_{1} \cdot x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}\end{array}\right]
   \end{aligned}
   $$

如上图所示: 第一列提公因式 $\left(x_{2}-x_{1}\right)$ 得
$$
1 \cdot\left(x_{2}-x_{1}\right) \times\left[\begin{array}{cccc}
1 & x_{3}-x_{1} & \ldots & x_{n}-x_{1} \\
x_{2} & x_{3}^{2}-x_{1} \cdot x_{3} & \ldots & x_{n}^{2}-x_{1} \cdot x_{n} \\
\ldots & \ldots & \ldots & \ldots \\
x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\
x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}
\end{array}\right]
$$
如上图所示: 第二列提公因式 $\left(x_{2}-x_{1}\right)$ 得:
$1 \cdot\left(x_{2}-x_{1}\right) \cdot\left(x_{3}-x_{1}\right) \times\left[\begin{array}{cccc}1 & 1 & \cdots & x_{n}-x_{1} \\ x_{2} & x_{3} & \cdots & x_{n}^{2}-x_{1} \cdot x_{n} \\ \ldots & \cdots & \cdots & \cdots \\ x_{2}^{n-3} & \cdots & \cdots & x_{n}^{n-2}-x_{1} \cdot x_{n}^{n-3} \\ x_{2}^{n-2} & \cdots & \cdots & x_{n}^{n-1}-x_{1} \cdot x_{n}^{n-2}\end{array}\right]$
依此类推：依此从第三列，第四列、第五列......第n列提公因式得:
$$
1 \cdot\left(x_{2}-x_{1}\right) \cdot\left(x_{3}-x_{1}\right) \cdot\left(x_{4}-x_{1}\right) \ldots \cdot\left(x_{n}-x_{1}\right) \times\left[\begin{array}{cccc}
1 & 1 & \ldots & 1 \\
x_{2} & x_{3} & \ldots & x_{n} \\
\ldots & \ldots & \cdots & \ldots \\
x_{2}^{n-3} & \ldots & \ldots & x_{n}^{n-3} \\
x_{2}^{n-2} & \ldots & \ldots & x_{n}^{n-2}
\end{array}\right]
$$
此时又是一个范德蒙行列式，按照如上的方法将此范德蒙行列式可以试着从第 $n$ 行开始，每个元 素都减去前一行元素的 $x_{2}$ 倍，然后提取公因式，如此循环，直至行列式化为数值 1 。通过对第 一轮的简化，依此计算得: $\prod_\limits{n \geq i>j \geq 1}=\left(x_{i}-x_{j}\right)$



5. 设 $\boldsymbol{A}=\left[\begin{array}{ccc}1 & 1 & 1 \\ 2 & 1 & -a \\ 1 & -2 & -3\end{array}\right] ，\boldsymbol{x}=\left[\begin{array}{l}x_{1} \\ x_{2} \\ x_{3}\end{array}\right] ，\quad \boldsymbol{b}=\left[\begin{array}{c}3 \\ 9 \\ -6\end{array}\right]$ $\boldsymbol{A} \boldsymbol{x}=\boldsymbol{b}$ 无解，求 $a$.
   [解答]

   方程组 $\boldsymbol{A} \boldsymbol{x}=\boldsymbol{b}$ 无解等价于 $\operatorname{rank}(\boldsymbol{A})<\operatorname{rank}(\boldsymbol{A} \mid \boldsymbol{b})$.

   因为
   $$
   \begin{gathered}
   \boldsymbol{A}=\left[\begin{array}{ccc}
   1 & 1 & 1 \\
   2 & 1 & -a \\
   1 & -2 & -3
   \end{array}\right] \stackrel{\frac{1}{2} r_{2}}{\longrightarrow}\left[\begin{array}{ccc}
   1 & 1 & 1 \\
   1 & \frac{1}{2} & -\frac{1}{2} a \\
   1 & -2 & -3
   \end{array}\right] \stackrel{r_{3}-r_{1}}{\longrightarrow} \\
   {\left[\begin{array}{ccc}
   1 & 1 & 1 \\
   0 & -\frac{1}{2} & -\frac{1}{2} a-1 \\
   0 & -3 & -4
   \end{array}\right] \stackrel{r_{2}-r_{1}}{\longrightarrow}\left[\begin{array}{ccc}
   1 & 1 & 1 \\
   0 & -\frac{1}{2} & -\frac{1}{2} a-1 \\
   0 & 0 & 3 a+2
   \end{array}\right]}
   \end{gathered}
   $$
   所以 $\operatorname{rank}(\boldsymbol{A})=\left\{\begin{array}{l}3, a \neq-\frac{2}{3} \\ 2, a=-\frac{2}{3}\end{array}\right.$.
   而同理可知，无论 $a$ 取何值，总有 $\operatorname{rank}(\boldsymbol{A} \mid \boldsymbol{b})=3$.
   故方程组 $\boldsymbol{A} \boldsymbol{x}=\boldsymbol{b}$ 无解当且仅当 $a=-\frac{2}{3}$.
   【另解】显然 $\boldsymbol{b}$ 不在 $\boldsymbol{A}$ 的列空间内. 故方程组无解等价于 $\operatorname{det} \boldsymbol{A}=-3 a-2=0$ ，即 $a=-\frac{2}{3}$

   

   2022年4月23日