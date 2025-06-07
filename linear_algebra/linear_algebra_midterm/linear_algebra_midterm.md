### Linear Algebra 期中专场

时间：2022年4月30日

Docx版本：[linear_algebra_midterm-docx.docx](./linear_algebra_midterm-docx.docx)

一、判断正误题(每小题2分，共10分)

1. Every matrix is row equivalent to a unique matrix in echelon form.  (T/F?)   False.

2. If $A$ is a $3{\times}3$ matrix, then $\operatorname{det} (2A) = 2\operatorname{det} (A)$.  (T/F?)  False.

3. If an augmented matrix $\left[\begin{array}{ll}A & \mathbf{b}\end{array}\right]$ is transformed into $\left[\begin{array}{ll}C & \mathbf{d}\end{array}\right]$ by elementary row operations, then the equations $A \mathbf{x}=\mathbf{b}$ and $C \mathbf{x}=\mathbf{d}$ have exactly the same solution sets.  (T/F?)   True.

4. Rank **A** = dim(Nul **A**).  (T/F?)   False.

5. If $A$ is $m \times n$ and the linear transformation $\mathbf{x} \mapsto A \mathbf{x}$ is onto, then $\operatorname{rank} A=m$.  (T/F?)  True.

   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(1).jpg)

二、填空题(每小题5分，共15分)

1. $\text { 若 }\left(\begin{array}{ll}
   2 & 5 \\
   1 & 3
   \end{array}\right) X=\left(\begin{array}{cc}
   4 & -6 \\
   2 & 1
   \end{array}\right) \text {, 则 } X=$________________________.

   1、若 $\left(\begin{array}{ll}2 & 5 \\ 1 & 3\end{array}\right) X=\left(\begin{array}{cc}4 & -6 \\ 2 & 1\end{array}\right)$, 则 $X=$______________________ 解答:
   $$
   X=\left(\begin{array}{ll}
   2 & 5 \\
   1 & 3
   \end{array}\right)^{-1}\left(\begin{array}{cc}
   4 & -6 \\
   2 & 1
   \end{array}\right)=\left(\begin{array}{cc}
   3 & -5 \\
   -1 & 2
   \end{array}\right)\left(\begin{array}{cc}
   4 & -6 \\
   2 & 1
   \end{array}\right)=\left(\begin{array}{cc}
   2 & -23 \\
   0 & 8
   \end{array}\right)
   $$



2. 已知向量组
   $$
   \boldsymbol{\alpha}_{1}=[1,-1,2]^{\mathrm{T}}, \boldsymbol{\alpha}_{2}=[0,3,1]^{\mathrm{T}}, \boldsymbol{\alpha}_{3}=[3,0,7]^{\mathrm{T}}
   $$
   与向量组
   $$
   \boldsymbol{\beta}_{1}=[1,-2,2]^{\mathrm{T}}, \boldsymbol{\beta}_{2}=[2,1,5]^{\mathrm{T}}, \boldsymbol{\beta}_{3}=[x, 3,3]^{\mathrm{T}}
   $$
   等秩, 则 $x=$____________________.



9.【解析】由 $\left[\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \boldsymbol{\alpha}_{3}\right]=\left[\begin{array}{ccc}1 & 0 & 3 \\ -1 & 3 & 0 \\ 2 & 1 & 7\end{array}\right] \rightarrow\left[\begin{array}{lll}1 & 0 & 3 \\ 0 & 3 & 3 \\ 0 & 1 & 1\end{array}\right] \rightarrow\left[\begin{array}{lll}1 & 0 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 0\end{array}\right]$, 知 $r\left(\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \boldsymbol{\alpha}_{3}\right)=2$. 由题设知, $r\left(\boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \boldsymbol{\beta}_{3}\right)=2$.
因
$$
\left[\boldsymbol{\beta}_{1}, \boldsymbol{\beta}_{2}, \boldsymbol{\beta}_{3}\right]=\left[\begin{array}{ccc}
1 & 2 & x \\
-2 & 1 & 3 \\
2 & 5 & 3
\end{array}\right] \rightarrow\left[\begin{array}{ccc}
1 & 2 & x \\
0 & 5 & 3+2 x \\
0 & 1 & 3-2 x
\end{array}\right] \rightarrow\left[\begin{array}{ccc}
1 & 2 & x \\
0 & 1 & 3-2 x \\
0 & 0 & -12+12 x
\end{array}\right]
$$
故$x = 1$.



3. 向量组$$
   \alpha_{1}=\left(\begin{array}{l}
   1 \\
   1 \\
   1
   \end{array}\right), \quad \alpha_{2}=\left(\begin{array}{l}
   0 \\
   2 \\
   5
   \end{array}\right), \quad \alpha_{3}=\left(\begin{array}{l}
   2 \\
   4 \\
   7
   \end{array}\right), \quad \alpha_{4}=\left(\begin{array}{l}
   1 \\
   2 \\
   0
   \end{array}\right)
   $$ 是线性_________________________(填相关或无关)的, 它的一个极大线性无关组是______________________________________.



​        相关 (因为向量个数大于向量维数)。 $\alpha_{1}, \alpha_{2}, \alpha_{4}$ 。因为 $\alpha_{3}=2 \alpha_{1}+\alpha_{2}$,
$$
A=\left|\begin{array}{lll}
\alpha_{1} & \alpha_{2} & \alpha_{4}
\end{array}\right| \neq 0 . \mid
$$

![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(2).jpg)


| 判断正误题 | 1    | 2    | 3    | 4    | 5    |
| :--------: | ---- | ---- | ---- | ---- | ---- |
|  你的判断  |      |      |      |      |      |

|  填空题  | 1    | 2    | 3(1) | 3(2) |
| :------: | ---- | ---- | ---- | ---- |
| 你的答案 |      |      |      |      |





三、计算与证明题(共75分)

1. (15分)求解下列齐次线性方程组:
   $$
   \left\{\begin{array}{l}
   3 x_{1}+4 x_{2}-5 x_{3}+7 x_{4}=0 \\
   2 x_{1}-3 x_{2}+3 x_{3}-2 x_{4}=0 \\
   4 x_{1}+11 x_{2}-13 x_{3}+16 x_{4}=0 \\
   7 x_{1}-2 x_{2}+x_{3}+3 x_{4}=0
   \end{array}\right.
   $$
   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(3).jpg)
   
   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(4).jpg)
   
2. (15分)求可逆矩阵 $\boldsymbol{P}$ 和对角矩阵 $\boldsymbol{D}$, 使 $\boldsymbol{A}=\boldsymbol{P D} \boldsymbol{P}^{-1}$.
   $$
   A=\left[\begin{array}{rrrr}
   5 & 0 & 0 & 0 \\
   0 & 5 & 0 & 0 \\
   1 & 4 & -3 & 0 \\
   -1 & -2 & 0 & -3
   \end{array}\right]
   $$
   
   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(4).jpg)
   
   ![img (5)](https://gitee.com/wwlccccc/images/raw/master/images/img%20(5).jpg)
   
3. (15分)设 $\mathcal{B}=\left\{\boldsymbol{b}_{1}, \boldsymbol{b}_{2}\right\}$ 和 $\mathcal{C}=\left\{\boldsymbol{c}_{1}, \boldsymbol{c}_{2}\right\}$ 是 $\mathbb{R}^{2}$ 的两个基, 求由 $\mathcal{B}$ 到 $\mathcal{C}$ 的坐标变换矩阵和由 $\mathcal{C}$ 到 $\mathcal{B}$ 的坐标变换矩阵.
   $$
   \boldsymbol{b}_{1}=\left[\begin{array}{l}
   7 \\
   5
   \end{array}\right], \boldsymbol{b}_{2}=\left[\begin{array}{r}
   -3 \\
   -1
   \end{array}\right], \boldsymbol{c}_{1}=\left[\begin{array}{r}
   1 \\
   -5
   \end{array}\right], \boldsymbol{c}_{2}=\left[\begin{array}{r}
   -2 \\
   2
   \end{array}\right]
   $$
   
   
   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(6).jpg)
   
4. (15分)$\text { 设 } A \text { 是 } n \times m \text { 矩阵, } \boldsymbol{B} \text { 是 } m \times n \text { 矩阵,其中 } n<m \text {, 若 } \boldsymbol{A B}=\boldsymbol{E} \text {, 证明 } \boldsymbol{B} \text { 的列向量线性无关. }$

   ![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(7).jpg)

5. (15分) 设

$$
V_{1}=\left\{\boldsymbol{x}=\left(x_{1}, x_{2}, \cdots, x_{n}\right)^{\mathrm{T}} \mid x_{1}, \cdots, x_{n} \in \mathbb{R} \text { 满足 } x_{1}+\cdots+x_{n}=0\right\} \text {, }
$$
$$
V_{2}=\left\{\boldsymbol{x}=\left(x_{1}, x_{2}, \cdots, x_{n}\right)^{\mathrm{T}} \mid x_{1}, \cdots, x_{n} \in \mathbb{R} \text { 满足 } x_{1}+\cdots+x_{n}=1\right\} \text {, }
$$
问 $V_{1}, V_{2}$ 是不是向量空间? 证明之.

![img (8)](https://gitee.com/wwlccccc/images/raw/master/images/img%20(8).jpg)

![](https://gitee.com/wwlccccc/images/raw/master/images/img%20(9).jpg)
