## T2

由于$U_1,\cdots,U_n$为在$(0,1)$中均匀分布的独立随机变量（$U_1,\cdots,U_n$同分布）
$$
\mu_X(t) = E[X(t)] = \frac{1}{n}\sum_{k=1}^{n}E[I(t, U_k)] = E[I(t, U_1)] = 1 \times P(U_1 \le t) + 0 \times P(U_1 > t) = P(U_1 \le t) = t,\qquad 0 \le t \le 1
$$
对于协方差有
$$
R_X(t, s) = \frac{1}{n^2}\sum_{i=1}^{n}\sum_{j=1}^{n}Cov[I(t, U_i), I(s, U_j)]
$$
注意到对于$i \neq j$
$$
E[I(t, U_i)I(s, U_j)] = 1 \times P(U_i \le t, U_j \le s) = P(U_i \le t)P(U_j \le s) = ts
$$
故
$$
Cov[I(t, U_i), I(s, U_j)] = E[I(t, U_i)I(s, U_j)] - E[I(t, U_i)]E[I(s, U_j)] = ts - ts = 0
$$
而对于$i = j (= k)$
$$
E[I(t, U_k)I(s, U_k)] = 1 \times P(U_k \le t, U_k \le s) = P(U_k \le min\{t, s \}) = min\{t, s \}
$$
从而
$$
Cov[I(t, U_k), I(s, U_k)] = E[I(t, U_k)I(s, U_k)] - E[I(t, U_k)]E[I(s, U_k)] = min\{t, s \} - ts
$$
故
$$
R_X(t, s) = \frac{1}{n^2}\sum_{k=1}^{n}Cov[I(t, U_k), I(s, U_k)] = \frac{1}{n}Cov[I(t, U_1), I(s, U_1)] = \frac{1}{n}(min\{t, s \} - ts) \qquad 0\le t, s \le 1
$$

## T4


$$
\mu_X(t) = E[X(t)] = E[X(t) - X(0)] = \lambda(t - 0) = \lambda t
$$

$$
R_X(t, s) = E[X(t)X(s)] - E[X(t)]E[X(s)]
$$

其中(不妨$s > t$)
$$
\begin{aligned}
	E[X(t)X(s)] &= E[(X(t) - X(0))(X(s) - X(t) + X(t) - X(0))] \newline
				&= E[(X(t) - X(0))^2] + E[(X(t) - X(0))(X(s) - X(t))]
\end{aligned}
$$
又注意到
$$
E[(X(t) - X(0))^2] = Var[X(t) - X(0)] + (E[X(t) - X(0)])^2 = (\lambda (t - 0)) + (\lambda (t - 0))^2 = \lambda t + (\lambda t)^2
$$
故
$$
E[X(t)X(s)] = \lambda t + (\lambda t)^2 + \lambda (t - 0) \times \lambda (s - t) = \lambda t(\lambda s + 1)
$$
（注意由先前假设$s > t$，所以实际上$E[X(t)X(s)] = \lambda min\{t, s \}(\lambda max\{t, s \} + 1)$）

从而
$$
R_X(t, s) = \lambda t(\lambda s + 1) - \lambda t \times \lambda s = \lambda t = \lambda min\{t, s \}
$$
由定义知不是宽平稳。

## T5

$$
\mu_Y(t) = E[Y(t)] = E[X(t + 1) - X(t)] = \lambda (t + 1 - t) = \lambda
$$

$$
\begin{aligned}
	R_Y(t, s) &= Cov[Y(t), Y(s)] = Cov[(X(t + 1) - X(t))(X(s + 1) - X(s))] \newline
			  &= Cov[(X(t + 1) , X(s + 1)] - Cov[(X(t + 1) , X(s)] - Cov[(X(t) , X(s + 1)] + Cov[(X(t) , X(s)] \newline
			  &= \lambda min\{t + 1, s + 1 \} - \lambda min\{t + 1, s \} - \lambda min\{t, s + 1 \} + \lambda min\{t, s \}
\end{aligned}
$$

从而
$$
R_Y(t, s) = \left\{
    \begin{aligned}
        & 0,                  &  0 \le t \le s - 1 \ 或 \ t \ge s + 1  \newline
        & \lambda(t - s + 1), &  s - 1 < t < s  \newline
        & \lambda(s - t + 1), &  s \le t < s + 1 
    \end{aligned}
\right.
$$
考虑二阶矩
$$
Var[Y(t)] = R_Y(t, t) = \lambda < \infin
$$
故是宽平稳的
