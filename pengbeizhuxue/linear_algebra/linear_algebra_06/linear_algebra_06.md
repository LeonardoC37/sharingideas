### Linear Algebra 06

时间：2022年5月12日

注意纠正Linear Algebra 05 中第三题的误区

(方阵可逆，非方阵的逆不存在，所以第二题求解坐标变换矩阵只能用方法三，不可以使用方法一和方法二)

矩阵的秩的相关定义的证明：

[常见的矩阵秩(不)等式及其各种证明 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/55206421)

去年附加题第二题的证明：

[康托洛维奇(Kantorovich)不等式的一种初等证明 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/271983329)

1. $\boldsymbol{A}$ 和 $\boldsymbol{B}$ 分别是 $m \times n$ 和 $n \times p$ 矩阵, 证明: $r(\boldsymbol{A B})+n \geq r(\boldsymbol{A})+r(\boldsymbol{B})$ 。

   提示：(1)设$A$是$m{\times}n$矩阵，$B$是$n{\times}s$矩阵，若$AB=O$，证明$rank(A)+rank(B){\leq}n$.

   (2)设$A$,$B$是行数相同的矩阵，$(A,B)$是由$A,B$并排组成的矩阵，证明$rank(A,B){\leq}rank(A)+rank(B)$.

   **引理1**

   设$A$是$m{\times}n$矩阵，$B$是$n{\times}s$矩阵，若$AB=O$，证明$rank(A)+rank(B){\leq}n$.

   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(1).jpg)

   [证明]

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

   **引理2**

   设$A$,$B$是行数相同的矩阵，$(A,B)$是由$A,B$并排组成的矩阵，证明$rank(A,B){\leq}rank(A)+rank(B)$.

   即是：分块矩阵的秩大于等于各分块的秩中的最大值，小于等于各分块的秩之和。

   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(2).jpg)

   [证明]

   设 $A$ 为 $s \times m$ 矩阵, $B$ 为 $s \times n$ 矩阵, 则 $\max \{\mathrm{r}(A), \mathrm{r}(B)\} \leq \mathrm{r}(A, B) \leq \mathrm{r}(A)+\mathrm{r}(B)$.
   (1) 因为 $A$ 和 $B$ 的子式也是分块矩阵 $(A, B)$ 的子式, 所以 $\mathrm{r}(A) \leq \mathrm{r}(A, B), \mathrm{r}(B) \leq \mathrm{r}(A, B)$.
   由此可见 $\max \{\mathrm{r}(A), \mathrm{r}(B)\} \leq \mathrm{r}(A, B)$ 成立.
   (2) 设 $P A^{\mathrm{T}}=U, Q B^{\mathrm{T}}=V$, 其中 $P, Q$ 可逆,
   $U, V$ 为行阶梯形矩阵, $\mathrm{r}(U)=\mathrm{r}\left(A^{\mathrm{T}}\right), \mathrm{r}(V)=\mathrm{r}\left(B^{\mathrm{T}}\right)$.
   于是 
   $$
   \mathrm{r}(\boldsymbol{A}, \boldsymbol{B})=\mathrm{r}(\boldsymbol{A}, \boldsymbol{B})^{\mathrm{T}}=\mathrm{r}\left[\begin{array}{l}
   A^{\mathrm{T}} \\
   B^{\mathrm{T}}
   \end{array}\right]=\mathrm{r}\left[\left(\begin{array}{ll}
   \boldsymbol{P} & \boldsymbol{O} \\
   \boldsymbol{O} & \boldsymbol{Q}
   \end{array}\right)\left(\begin{array}{l}
   A^{\mathrm{T}} \\
   B^{\mathrm{T}}
   \end{array}\right)\right]
   =\mathbf{r}\left[\begin{array}{l}
   U \\
   V
   \end{array}\right] \leq \mathbf{r}\left(A^{\mathrm{T}}\right)+\mathbf{r}\left(B^{\mathrm{T}}\right)=\mathbf{r}(A)+\mathbf{r}(B)
   $$
   **本题证明**

   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(3).jpg)

   记 $B=\left(\beta_{1}, \beta_{2}, \ldots, \beta_{p}\right)$ ，其中 $\beta_{i}(i=1,2, \ldots, p)$ 是 $B$ 的列向量。那么
   $$
   A B=\left(A \beta_{1}, A \beta_{2}, \ldots, A \beta_{p}\right)
   $$
   设 $A \beta_{r_{1}}, A \beta_{r_{2}}, \ldots, A \beta_{r_{s}}$ 是 $A B$ 的一个极大线性无关组，在剩下的 $p-s$ 个向量中的任 意一个向量 $\beta_{j}$ ，我们都有 $A \beta_{j}=k_{j_{1}} A \beta_{r_{1}}+\ldots+k_{j_{s}} A \beta_{r_{s}}$ ，因此
   $$
   \hat{\beta}_{j}=\beta_{j}-\sum_{i=1}^{s} k_{j_{i}} \beta_{r_{i}}
   $$
   是方程 $A X=0$ 的解，这些 $p-s$ 个解向量 $\hat{\beta}_{j_{1}}, \hat{\beta}_{j_{2}}, \ldots, \hat{\beta}_{j_{p-s}}$ 构成的矩阵，我们有
   $$
   \operatorname{rank}\left(\hat{\beta}_{j_{1}}, \hat{\beta}_{j_{2}}, \ldots, \hat{\beta}_{j_{p-s}}\right) \leq n-\operatorname{rank}(A)
   $$
   而
   $$
   \operatorname{rank}(B)=\operatorname{rank}\left(\beta_{1}, \beta_{2}, \ldots, \beta_{p}\right)=\operatorname{rank}\left(\beta_{r_{1}}, \ldots, \beta_{r_{s}}, \hat{\beta}_{j_{1}}, \hat{\beta}_{j_{2}}, \ldots, \hat{\beta}_{j_{p-s}}\right)
   $$
   因此
   $$
   \operatorname{rank}(B) \leq \operatorname{rank}\left(\beta_{r_{1}}, \ldots, \beta_{r_{s}}\right)+\operatorname{rank}\left(\hat{\beta}_{j_{1}}, \hat{\beta}_{j_{2}}, \ldots, \hat{\beta}_{j_{p-s}}\right) \leq \operatorname{rank}(A B)+n-\operatorname{rank}(A)
   $$
   故命题成立。

2. 已知二次型 $f\left(x_{1}, x_{2}, x_{3}\right)=x_{1}^{2}+5 x_{2}^{2}+5 x_{3}^{2}+2 x_{1} x_{2}-4 x_{1} x_{3}$
   (1) 写出二次型 $f$ 的矩阵表达式.
   (2) 用正交变换把二次型 $f$ 化成标准形, 并写出相应的正交矩阵.
   (3) 当 $\boldsymbol{x}^{T} \boldsymbol{x}=2$ 时, $f\left(x_{1}, x_{2}, x_{3}\right)$ 的极大值.

   [解答]

   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(4).jpg)
   
   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(5).jpg)
   
   (1) $f$ 的矩阵表示为
   $$
   f\left(x_{1}, x_{2}, x_{3}\right)=\boldsymbol{x}^{T} \boldsymbol{A} \boldsymbol{x}=\left[x_{1}, x_{2}, x_{3}\right]\left[\begin{array}{ccc}
   1 & 1 & -2 \\
   1 & 5 & 0 \\
   -2 & 0 & 5
   \end{array}\right]\left[\begin{array}{l}
   x_{1} \\
   x_{2} \\
   x_{3}
   \end{array}\right]
   $$
   (2) 由矩阵 $\boldsymbol{A}$ 的特征多项式
   $$
   \begin{gathered}
   |\lambda \boldsymbol{E}-\boldsymbol{A}|\left|\begin{array}{ccc}
   \lambda-1 & -1 & 2 \\
   -1 & \lambda-5 & 0 \\
   2 & 0 & \lambda-5
   \end{array}\right|=\left|\begin{array}{ccc}
   \lambda-1 & -1 & 2 \\
   -1 & \lambda-5 & 0 \\
   0 & 2(\lambda-5) & \lambda-5
   \end{array}\right| \\
   =\left|\begin{array}{ccc}
   \lambda-1 & -5 & 2 \\
   -1 & \lambda-5 & 0 \\
   0 & 0 & \lambda-5
   \end{array}\right|=(\lambda-5)\left(\lambda^{2}-6 \lambda\right)
   \end{gathered}
   $$
   得到 $\boldsymbol{A}$ 的特征值是 $0,5,6$.
   (1) 当 $\lambda=0$ 时,由 $(0 \boldsymbol{E}-\boldsymbol{A}) \boldsymbol{x}=\mathbf{0}$, 即 $\left[\begin{array}{ccc}-1 & -1 & 2 \\ -1 & -5 & 0 \\ 0 & 2 & 1\end{array}\right] \rightarrow\left[\begin{array}{ccc}1 & 5 & 0 \\ 0 & 2 & 1 \\ 0 & 0 & 0\end{array}\right]$
   得基础解系 $\boldsymbol{\alpha}_{1}=[5,-1,2]^{T}$, 即 $\lambda=0$ 的特征向量.
   
   (2) 当 $\lambda=5$ 时, 由 $(5 E-A) x=0$, 即
   $$
   \left[\begin{array}{ccc}
   4 & -1 & 2 \\
   -1 & 0 & 0 \\
   2 & 0 & 0
   \end{array}\right] \rightarrow\left[\begin{array}{ccc}
   1 & 0 & 0 \\
   0 & -1 & 2 \\
   0 & 0 & 0
   \end{array}\right]
   $$
   得基础解系, $\boldsymbol{\alpha}_{2}=[0,2,1]^{T}$, 即 $\lambda=5$ 的特征向量.
   (3) 当 $\lambda=6$ 时, 由 $(6 \boldsymbol{E}-\boldsymbol{A}) \boldsymbol{x}=0$, 即
   $$
   \left[\begin{array}{ccc}
   5 & -1 & 2 \\
   -1 & 1 & 0 \\
   2 & 0 & 1
   \end{array}\right] \rightarrow\left[\begin{array}{ccc}
   1 & -1 & 0 \\
   0 & 2 & 1 \\
   0 & 0 & 0
   \end{array}\right]
   $$
   得基础解系 $\boldsymbol{\alpha}_{3}=[1,1,-2]^{T}$, 即 $\lambda=6$ 的特征向量.
   
   对于实对称矩阵, 特征值不同, 特征向量已正交, 故只需单位化, 有
   $$
   \boldsymbol{\gamma}_{1}=\frac{1}{\sqrt{30}}\left[\begin{array}{r}
   5 \\
   -1 \\
   2
   \end{array}\right], \boldsymbol{\gamma}_{2}=\frac{1}{\sqrt{5}}\left[\begin{array}{l}
   0 \\
   2 \\
   1
   \end{array}\right], \boldsymbol{\gamma}_{3}=\frac{1}{\sqrt{6}}\left[\begin{array}{r}
   1 \\
   1 \\
   -2
   \end{array}\right]
   $$
   那么, 令
   $$
   \boldsymbol{P}=\left(\boldsymbol{\gamma}_{1}, \boldsymbol{\gamma}_{2}, \boldsymbol{\gamma}_{3}\right)=\left[\begin{array}{ccc}
   \frac{5}{\sqrt{30}} & 0 & \frac{1}{\sqrt{6}} \\
   -\frac{1}{\sqrt{30}} & \frac{2}{\sqrt{5}} & \frac{1}{\sqrt{6}} \\
   \frac{2}{\sqrt{30}} & \frac{1}{\sqrt{5}} & -\frac{2}{\sqrt{6}}
   \end{array}\right]
   $$
   经正交变换 $\boldsymbol{x}=\boldsymbol{P y}$, 二次型化为标准形
   $$
   f\left(x_{1}, x_{2}, x_{3}\right)=\boldsymbol{x}^{T} \boldsymbol{A} \boldsymbol{x}=\boldsymbol{y}^{T} \boldsymbol{A} \boldsymbol{y}=5 y_{2}^{2}+6 y_{3}^{2}
   $$
   ![](https://gitee.com/wwlccccc/images/raw/master/images/image%20(6).jpg)
   
   (3) $\boldsymbol{x}^{T} \boldsymbol{x}=(\boldsymbol{P} \boldsymbol{y})^{T}(\boldsymbol{P} \boldsymbol{y})=\boldsymbol{y}^{T} \boldsymbol{P}^{T} \boldsymbol{P} \boldsymbol{y}=\boldsymbol{y}^{T} \boldsymbol{y}=y_{1}^{2}+y_{2}^{2}+y_{3}^{2}=2$
   $$
   \boldsymbol{x}^{T} \boldsymbol{A} \boldsymbol{x}=5 y_{2}^{2}+6 y_{3}^{2} \leqslant 6\left(y_{1}^{2}+y_{2}^{2} y_{3}^{2}\right)
   $$
   所以, $f_{\text {max }}=12$.