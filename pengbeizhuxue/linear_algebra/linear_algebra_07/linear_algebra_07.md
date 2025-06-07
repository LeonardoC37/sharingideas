### Linear Algebra 07

时间：2022年5月19日

1. 解方程组.
   $$
   \left\{\begin{array}{l}
   2 x_{1}-2 x_{2}+x_{3}-x_{4}+x_{5}=1 \\
   x_{1}+2 x_{2}-x_{3}+x_{4}-2 x_{5}=1 \\
   4 x_{1}-10 x_{2}+5 x_{3}-5 x_{4}+7 x_{5}=1 \\
   2 x_{1}-14 x_{2}+7 x_{3}-7 x_{4}+11 x_{5}=-1
   \end{array}\right.
   $$
   
   
   
   
   [解答]
   
   ![](img (1).jpg)
   
   对增广矩阵作初等变换化为阶梯型，有
   $$
   \overline{\boldsymbol{A}}=\left[\begin{array}{ccccc:c}
   2 & -2 & 1 & -1 & 1 & 1 \\
   1 & 2 & -1 & 1 & -2 & 1 \\
   4 & -10 & 5 & -5 & 7 & 1 \\
   2 & -14 & 7 & -7 & 11 & -1
   \end{array}\right] \rightarrow\left[\begin{array}{ccccc:c}
   1 & 2 & -1 & 1 & -2 & 1 \\
   2 & -2 & 1 & -1 & 1 & 1 \\
   4 & -10 & 5 & -5 & 7 & 1 \\
   2 & -14 & 7 & -7 & 11 & -1
   \end{array}\right]
   $$
   $$
   \rightarrow\left[\begin{array}{ccccc:c}
   1 & 2 & -1 & 1 & -2 & 1 \\
   0 & -6 & 3 & -3 & 5 & -1 \\
   0 & -18 & 9 & -9 & 15 & -3 \\
   0 & -18 & 9 & -9 & 15 & -3
   \end{array}\right] \rightarrow\left[\begin{array}{ccccc:c}
   1 & 2 & -1 & 1 & -2 & 1 \\
   0 & 6 & -3 & 3 & -5 & 1 \\
   0 & 0 & 0 & 0 & 0 & 0 \\
   0 & 0 & 0 & 0 & 0 & 0
   \end{array}\right]
   $$
   由于 $r(\boldsymbol{A})=r(\overline{\boldsymbol{A}})$ 方程组有解,其同解的线性方程组是
   移项,得
   $$
   \begin{aligned}
   &\left\{\begin{array}{l}
   x_{1}+2 x_{2}-x_{3}+x_{4}-2 x_{5}=1 \\
   6 x_{2}-3 x_{3}+3 x_{4}-5 x_{5}=1
   \end{array}\right. \\
   &\left\{\begin{array}{c}
   x_{1}+2 x_{2}=1+x_{3}-x_{4}+2 x_{5} \\
   6 x_{2}=1+3 x_{3}-3 x_{4}+5 x_{5}
   \end{array}\right.
   \end{aligned}
   $$
   (1) 先求特解 $\boldsymbol{\alpha}$, 只要取 $x_{3}=x_{4}=x_{5}=0$ 即可, 于是
   $$
   \boldsymbol{\alpha}=\left[\frac{2}{3}, \frac{1}{6}, 0,0,0\right]^{\mathrm{T}} \text {. }
   $$
   (2) 再求出组的基础解系 (需把方程组的常数项换成零), 得
   $$
   \left\{\begin{array}{c}
   x_{1}+2 x_{2}=x_{3}-x_{4}+2 x_{5} \\
   6 x_{2}=3 x_{3}-3 x_{4}+5 x_{5}
   \end{array}\right.
   $$
   此时 $n-r(\boldsymbol{A})=5-2=3, x_{3}, x_{4}, x_{5}$ 是自由变量.
   $$
   \begin{aligned}
   &\text { 令 } x_{3}=1, x_{4}=0, x_{5}=0 \text {, 得 } \boldsymbol{\eta}_{1}=\left[0, \frac{1}{2}, 1,0,0\right]^{\mathrm{T}} \text {. } \\
   &\text { 令 } x_{3}=0, x_{4}=1, x_{5}=0 \text {, 得 } \boldsymbol{\eta}_{2}=\left[0,-\frac{1}{2}, 0,1,0\right]^{\mathrm{T}} \text {. } \\
   &\text { 令 } x_{3}=0, x_{4}=0, x_{5}=1 \text {, 得 } \boldsymbol{\eta}_{3}=\left[\frac{1}{3}, \frac{5}{6}, 0,0,1\right]^{\mathrm{T}} \text {, }
   \end{aligned}
   $$
   故方程组的通解是 $\boldsymbol{\alpha}+k_{1} \boldsymbol{\eta}_{1}+k_{2} \boldsymbol{\eta}_{2}+k_{3} \boldsymbol{\eta}_{3}\left(k_{1}, k_{2}, k_{3}\right.$ 为任意常数).
   **解题要点**: 本题主要考察线性方程组的基本解题步骤。
   
2. 求解下列矩阵$X$.
   $$
   \boldsymbol{X}\left(\begin{array}{ccc}
   1 & -2 & 0 \\
   2 & 1 & 3 \\
   0 & 2 & 1
   \end{array}\right)=\left(\begin{array}{ccc}
   1 & -1 & 1 \\
   2 & -3 & 1 \\
   3 & -4 & 1
   \end{array}\right)
   $$
   
   [解答]
   
   ![](img (2).jpg)
   
   将矩阵方程 $X A=B$ 两边同时取转置, 化成 $A^{\mathrm{T}} X^{\mathrm{T}}=B^{\mathrm{T}}$, 通过有限次初等行变抰将 $\left(A^{\mathrm{T}}, B^{\mathrm{T}}\right) \rightarrow(\boldsymbol{I}, \boldsymbol{Y})$, 则 $\boldsymbol{X}=\boldsymbol{Y}^{\mathrm{T}}$ 是所求的解 $B A^{-1}$.
   $$
   \left(\begin{array}{cccccc}
   1 & 2 & 0 & 1 & 2 & 3 \\
   -2 & 1 & 2 & -1 & -3 & -4 \\
   0 & 3 & 1 & 1 & 1 & 1
   \end{array}\right) \stackrel{2(1)+(2)}{\longrightarrow}\left(\begin{array}{llllll}
   1 & 2 & 0 & 1 & 2 & 3 \\
   0 & 5 & 2 & 1 & 1 & 2 \\
   0 & 3 & 1 & 1 & 1 & 1
   \end{array}\right)
   $$
   $$
   \stackrel{-\frac{3}{5}(2)+(3),-5(3)}{\longrightarrow}\left(\begin{array}{cccccc}
   1 & 2 & 0 & 1 & 2 & 3 \\
   0 & 5 & 2 & 1 & 1 & 2 \\
   0 & 0 & 1 & -2 & -2 & 1
   \end{array}\right) \stackrel{-2(3)+(2)}{\longrightarrow}
   $$
   $$
   \left(\begin{array}{cccccc}
   1 & 2 & 0 & 1 & 2 & 3 \\
   0 & 5 & 0 & 5 & 5 & 0 \\
   0 & 0 & 1 & -2 & -2 & 1
   \end{array}\right) \stackrel{\frac{1}{5}(2),-2(2)+(1)}{\longrightarrow}\left(\begin{array}{cccccc}
   1 & 0 & 0 & -1 & 0 & 3 \\
   0 & 1 & 0 & 1 & 1 & 0 \\
   0 & 0 & 1 & -2 & -2 & 1
   \end{array}\right)
   $$
   $$
   \boldsymbol{X}=\left(\begin{array}{ccc}
   -1 & 1 & -2 \\
   0 & 1 & -2 \\
   3 & 0 & 1
   \end{array}\right)
   $$
   
3. $\text { 将二次型 } 2 x_{3}^{2}-2 x_{1} x_{2}+2 x_{1} x_{3}-2 x_{2} x_{3} \text { 通过正交变换化为标准形, 并写出所用正交变换. }$

   [解答]![](img (3).jpg)

   ![](img (4).jpg)

   二次型矩阵 $\boldsymbol{A}=\left[\begin{array}{ccc}0 & -1 & 1 \\ -1 & 0 & -1 \\ 1 & -1 & 2\end{array}\right]$. 由特征多项式
   $$
   |\lambda \boldsymbol{E}-\boldsymbol{A}|\left|\begin{array}{ccc}
   \lambda & 1 & -1 \\
   1 & \lambda & 1 \\
   -1 & 1 & \lambda-2
   \end{array}\right|=\left|\begin{array}{ccc}
   \lambda+1 & 0 & 0 \\
   1 & \lambda-1 & 1 \\
   -1 & 2 & \lambda-2
   \end{array}\right|=(\lambda+1)\left(\lambda^{2}-3 \lambda\right),
   $$
   得到 $\boldsymbol{A}$ 的特征值是 $3,-1,0$.
   对 $\lambda=3$, 由 $(3 \boldsymbol{E}-\boldsymbol{A}) \boldsymbol{x}=\mathbf{0}$, 即 $\left[\begin{array}{ccc}3 & 1 & -1 \\ 1 & 3 & 1 \\ -1 & 1 & 1\end{array}\right]=\left[\begin{array}{ccc}1 & 3 & 1 \\ & 2 & 1 \\ & 0\end{array}\right]$, 解得 $\boldsymbol{\alpha}_{1}=(1,-1,2)^{T}$. 类似地, 对 $\lambda=-1, \boldsymbol{\alpha}_{2}=(1,1,0)^{T} ; \lambda=0$ 时, $\boldsymbol{\alpha}_{3}=(-1,1,1)^{T}$. 特征值无重根, 仅需单位化: $\boldsymbol{\gamma}_{1}=\frac{\boldsymbol{\alpha}}{\left\|\boldsymbol{\alpha}_{1}\right\|}=\frac{1}{\sqrt{6}}\left[\begin{array}{r}1 \\ -1 \\ 2\end{array}\right], \boldsymbol{\gamma}_{2}=\frac{\boldsymbol{\alpha}_{2}}{\left\|\boldsymbol{\alpha}_{2}\right\|}=\frac{1}{\sqrt{2}}\left[\begin{array}{l}1 \\ 1 \\ 0\end{array}\right], \gamma_{3}=\frac{\boldsymbol{\alpha}_{3}}{\left\|\boldsymbol{\alpha}_{3}\right\|}=\frac{1}{\sqrt{3}}\left[\begin{array}{r}-1 \\ 1 \\ 1\end{array}\right] .$ 构造正交矩阵 $\boldsymbol{C}=\left[\begin{array}{ccc}\frac{1}{\sqrt{6}} & \frac{1}{\sqrt{2}} & -\frac{1}{\sqrt{3}} \\ -\frac{1}{\sqrt{6}} & \frac{1}{\sqrt{2}} & \frac{1}{\sqrt{3}} \\ \frac{2}{\sqrt{6}} & 0 & \frac{1}{\sqrt{3}}\end{array}\right]$, 那么令 $\boldsymbol{x}=\boldsymbol{C y}$, 二次型 $\boldsymbol{x}^{T} \boldsymbol{A} \boldsymbol{x}=3 y_{1}^{2}-y_{2}^{2}$ 为所求标准形.

4. 设 $\boldsymbol{\alpha}_{i}=\left[a_{i 1}, a_{i 2}, \cdots, a_{i n}\right]^{\mathrm{T}}(i=1,2, \cdots, r, r<n)$ 是 $n$ 维实向量,且 $\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \cdots, \boldsymbol{\alpha}_{r}$ 线性无关. 已知 $\boldsymbol{\beta}=\left[b_{1}, b_{2}, \cdots, b_{n}\right]^{\mathrm{T}}$ 是线性方程组
   $$
   \left\{\begin{array}{l}
   a_{11} x_{1}+a_{12} x_{2}+\cdots+a_{1 n} x_{n}=0 \\
   a_{21} x_{1}+a_{22} x_{2}+\cdots+a_{2 n} x_{n}=0 \\
   \cdots \cdots \cdots \cdots \\
   a_{r 1} x_{1}+a_{r 2} x_{2}+\cdots+a_{m} x_{n}=0
   \end{array}\right.
   $$
   的非零解向量, 试判断向量组 $\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \cdots, \boldsymbol{\alpha}_{r}, \boldsymbol{\beta}$ 的线性相关性.
   
   [解答]![](img (5).jpg)
   
   (用定义, 同乘) 设 $k_{1} \boldsymbol{\alpha}_{1}+k_{2} \boldsymbol{\alpha}_{2}+\cdots+k_{r} \boldsymbol{\alpha}_{r}+l \boldsymbol{\beta}=\mathbf{0}$
   因为 $\boldsymbol{\beta}$ 为齐次方程组的非零解, 有
   $$
   \left\{\begin{array}{l}
   a_{11} b_{1}+a_{12} b_{2}+\cdots+a_{1 n} x_{n}=0 \\
   a_{21} b_{1}+a_{22} b_{2}+\cdots+a_{2 n} b_{n}=0 \\
   \cdots \cdots \cdots \cdots \\
   a_{r 1} b_{1}+a_{r 2} b_{2}+\cdots+a_{m} b_{n}=0
   \end{array}\right.(1)
   $$
   即 $\boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\alpha}_{1}=0, \boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\alpha}_{2}=0, \cdots, \boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\alpha}_{r}=0$.
   用 $\boldsymbol{\beta}^{\mathrm{T}}$ 左乘 (1) 式两端, 并把 $\boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\beta}_{i}=0$ 代人, 得
   $$
   l\boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\beta}=0,(2)
   $$
   因为 $\boldsymbol{\beta} \neq \mathbf{0}$, 有 $\boldsymbol{\beta}^{\mathrm{T}} \boldsymbol{\beta}=b_{1}^{1}+b_{2}^{2}+\cdots+b_{n}^{2}>0$, 故必有 $l=0$, 代人 (1) 式, 得
   $$
   k_{1} \boldsymbol{\alpha}_{1}+k_{2} \boldsymbol{\alpha}_{2}+\cdots+k_{r} \boldsymbol{\alpha}_{r}=\mathbf{0},(3)
   $$
   因为 $\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \cdots, \boldsymbol{\alpha}_{r}$ 线性无关, 由 (3) 知
   $$
   k_{1}=0, k_{2}=0, \cdots, k_{r}=0
   $$
   从而向量组 $\boldsymbol{\alpha}_{1}, \boldsymbol{\alpha}_{2}, \cdots, \boldsymbol{\alpha}_{r}, \boldsymbol{\beta}$ 线性无关.
   解题要点: 本题主要考察用定义证明线性相关性.