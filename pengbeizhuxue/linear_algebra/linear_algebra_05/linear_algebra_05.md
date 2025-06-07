### Linear Algebra 05

时间：2022年5月5日



1. a. A matrix *A* is orthogonally diagonalizable if and only if *A* is symmetric. (T/F?) True

   ![](img (6).jpg)

   b. The set of all vectors in $\mathbb{R}^{n}$ orthogonal to one fixed vector is a subspace of $\mathbb{R}^{n}$.(T/F?) True

   [解答]$\mathbf{k}$. True. This is a special case of the statement in the box following Example 6 in Section $6.1$ (and proved in Exercise 30 of Section 6.1).

   ![](img (1).jpg)

2. Find a $\mathrm{QR}$ factorization of $A=\left[\begin{array}{ccc}1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 1 & 1 \\ 1 & 1 & 1\end{array}\right]$.

   ![](img (2).jpg)

   [解答]

   The columns of $A$ are the vectors $\mathbf{x}_{1}, \mathbf{x}_{2}$, and $\mathbf{x}_{3}$ in Example 2 . An orthogonal basis for $\operatorname{Col} A=\operatorname{Span}\left\{\mathbf{x}_{1}, \mathbf{x}_{2}, \mathbf{x}_{3}\right\}$ was found in that example:
   $$
   \mathbf{v}_{1}=\left[\begin{array}{l}
   1 \\
   1 \\
   1 \\
   1
   \end{array}\right], \quad \mathbf{v}_{2}^{\prime}=\left[\begin{array}{r}
   -3 \\
   1 \\
   1 \\
   1
   \end{array}\right], \quad \mathbf{v}_{3}=\left[\begin{array}{c}
   0 \\
   -2 / 3 \\
   1 / 3 \\
   1 / 3
   \end{array}\right]
   $$
   To simplify the arithmetic that follows, scale $\mathbf{v}_{3}$ by letting $\mathbf{v}_{3}^{\prime}=3 \mathbf{v}_{3}$. Then normalize the three vectors to obtain $\mathbf{u}_{1}, \mathbf{u}_{2}$, and $\mathbf{u}_{3}$, and use these vectors as the columns of $Q$ :
   $$
   Q=\left[\begin{array}{rrc}
   1 / 2 & -3 / \sqrt{12} & 0 \\
   1 / 2 & 1 / \sqrt{12} & -2 / \sqrt{6} \\
   1 / 2 & 1 / \sqrt{12} & 1 / \sqrt{6} \\
   1 / 2 & 1 / \sqrt{12} & 1 / \sqrt{6}
   \end{array}\right]
   $$

   By construction, the first $k$ columns of $Q$ are an orthonormal basis of $S$ pan $\left\{\mathbf{x}_{1}, \ldots, \mathbf{x}_{k}\right\}$. From the proof of Theorem $12, A=Q R$ for some $R$. To find $R$, observe that $Q^{T} Q=I$, because the columns of $Q$ are orthonormal. Hence
   $$
   Q^{T} A=Q^{T}(Q R)=I R=R
   $$
   and
   $$
   \begin{aligned}
   R &=\left[\begin{array}{clll}
   1 / 2 & 1 / 2 & 1 / 2 & 1 / 2 \\
   -3 / \sqrt{12} & 1 / \sqrt{12} & 1 / \sqrt{12} & 1 / \sqrt{12} \\
   0 & -2 / \sqrt{6} & 1 / \sqrt{6} & 1 / \sqrt{6}
   \end{array}\right]\left[\begin{array}{lll}
   1 & 0 & 0 \\
   1 & 1 & 0 \\
   1 & 1 & 1 \\
   1 & 1 & 1
   \end{array}\right] \\
   &=\left[\begin{array}{ccc}
   2 & 3 / 2 & 1 \\
   0 & 3 / \sqrt{12} & 2 / \sqrt{12} \\
   0 & 0 & 2 / \sqrt{6}
   \end{array}\right]
   \end{aligned}
   $$

3. 设 $\alpha_{1}=(1,2,1,0)^{T} ， \alpha_{2}=(1,1,1,2)^{T} ， \alpha_{3}=(3,4,3,4)^{T}$ ， $\alpha_{4}=(1,1,2,1)^{T} ， \alpha_{5}=(4,5,6,4)^{T}$ 是实向量空间 $\mathbb{R}^{4}$ 中的一个向量组， $L$ 是该向量组生成的 $\mathbb{R}^{4}$ 的子空间.
   (1) 试证明: $\beta_{1}=\left\{\alpha_{1}, \alpha_{2}, \alpha_{4}\right\}$ 和 $\beta_{2}=\left\{\alpha_{2}, \alpha_{3}, \alpha_{5}\right\}$ 分别是 $L$ 的两组基;
   (2) 求从基 $\beta_{1}$ 到基 $\beta_{2}$ 的过渡矩阵.

   ![](img (3).jpg)
   
   [解答] (1) 要证明 $\beta=\left\{\alpha_{1}, \alpha_{2}, \alpha_{3}, \alpha_{4}, \alpha_{5}\right\}$ 的某个子集 $\beta^{\prime}$ 是 $L$ 的一组基，只需证明在 $\beta$ 中但不在 $\beta^{\prime}$ 中的向量能被 $\beta^{\prime}$ 中的向量线性表示出.
   设 $\left\{\begin{array}{l}\alpha_{3}=a_{11} \alpha_{1}+a_{12} \alpha_{2}+a_{13} \alpha_{4} \\ \alpha_{5}=a_{21} \alpha_{1}+a_{22} \alpha_{2}+a_{23} \alpha_{4}\end{array}\right.$ ，解线性方程组可得（具体过程略) $\alpha_{3}=\alpha_{1}+2 \alpha_{2}, \quad \alpha_{5}=\alpha_{1}+\alpha_{2}+2 \alpha_{4}$,
   所以 $\left\{\alpha_{1}, \alpha_{2}, \alpha_{4}\right\}$ 是 $L$ 的一组基.
   由此知， $\operatorname{dim} L=3$ ，所以要证明 $\left\{\alpha_{2}, \alpha_{3}, \alpha_{5}\right\}$ 是 $L$ 的一组基，只需证明该集合线性无 关，
   只需证明矩阵 $A:=\left(\begin{array}{lll}\alpha_{2} & \alpha_{3} & \alpha_{5}\end{array}\right)=\left(\begin{array}{lll}1 & 3 & 4 \\ 1 & 4 & 5 \\ 1 & 3 & 6 \\ 2 & 4 & 4\end{array}\right)$ 满秩.
   
   通过初等行变换，可将 $A$ 化为 $\left(\begin{array}{lll}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0\end{array}\right)$ ，说明矩阵 $A$ 的秩为 3 ，得证.
   
   ![](img (4).jpg)
   
   **[注意]其中方法一和方法二用到了逆矩阵，要求对应的矩阵可逆，本题的矩阵不可逆，所以不可以采用方法一和方法二，而方法三可以有效解答本题。**
   
   (2) 设 $I$ 是 $L$ 上的恒等变换，则所求过渡矩阵为 $Q=[I]_{\beta_{2}}^{\beta_{1}}$.
   由 (1) 知， $\alpha_{2}=\alpha_{2}, \alpha_{3}=\alpha_{1}+2 \alpha_{2} ， \alpha_{5}=\alpha_{1}+\alpha_{2}+2 \alpha_{4}$ ，
   所以过渡矩阵为 $Q=\left(\begin{array}{lll}0 & 1 & 1 \\ 1 & 2 & 1 \\ 0 & 0 & 2\end{array}\right)$.
   
4. 设 $A$ 为 $n$ 阶矩阵, $\lambda_{1}$ 和 $\lambda_{2}$ 是 $A$ 的两个不同的特征值, $x_{1}, x_{2}$ 是 $A$ 的分别属于 $\lambda_{1}$ 和 $\lambda_{2}$ 的特征 向量. 证明: $x_{1}+x_{2}$ 不是 $\boldsymbol{A}$ 的特征向量.

   ![](img (5).jpg)

   [解答]反证法. 
   
   设 $x_{1}+x_{2}$ 是 $\boldsymbol{A}$ 的特征向量, 则存在数 $\lambda$, 使得 $\boldsymbol{A}\left(\boldsymbol{x}_{1}+\boldsymbol{x}_{2}\right)=\lambda\left(\boldsymbol{x}_{1}+\boldsymbol{x}_{2}\right)$, 则
   $$
   \left(\lambda-\lambda_{1}\right) x_{1}+\left(\lambda-\lambda_{2}\right) x_{2}=\mathbf{0} .
   $$
   因为 $\lambda_{1} \neq \lambda_{2}$, 所以 $x_{1}, x_{2}$ 线性无关, 则 $\left\{\begin{array}{l}\lambda-\lambda_{1}=0, \\ \lambda-\lambda_{2}=0\end{array} \Rightarrow \lambda_{1}=\lambda_{2}\right.$. 矛盾, 故得证.