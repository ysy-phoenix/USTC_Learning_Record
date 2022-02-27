## 练习 1

列真值表，无需赘述。

### 7&deg;

| ($\neg$ |  p   | $\vee$ |  q)  | $\rightarrow$ | ($\neg$ |  q   | $\wedge$ |  r)  |
| :-----: | :--: | :----: | :--: | :-----------: | :-----: | :--: | :------: | :--: |
|    0    |  1   |   0    |  1   |       1       |    0    |  1   |    0     |  1   |
|   00    |  1   |   0    |  1   |       1       |    0    |  1   |    0     |  0   |
|    0    |  1   |   0    |  0   |       1       |    1    |  0   |    1     |  1   |
|    0    |  1   |   0    |  0   |       1       |    1    |  0   |    0     |  0   |
|    1    |  0   |   1    |  1   |       0       |    0    |  1   |    0     |  1   |
|    1    |  0   |   1    |  1   |       0       |    0    |  1   |    0     |  0   |
|    1    |  0   |   0    |  0   |       1       |    1    |  0   |    1     |  1   |
|    1    |  0   |   0    |  0   |       1       |    1    |  0   |    0     |  0   |

### 8&deg;

|  (p  | $\rightarrow$ |  q)  | $\rightarrow$ |  (p  | $\rightarrow$ |  r)  |
| :--: | :-----------: | :--: | :-----------: | :--: | :-----------: | :--: |
|  1   |       1       |  1   |       1       |  1   |       1       |  1   |
|  1   |       1       |  1   |       0       |  1   |       0       |  0   |
|  1   |       0       |  0   |       1       |  1   |       1       |  1   |
|  1   |       0       |  0   |       1       |  1   |       0       |  0   |
|  0   |       1       |  1   |       1       |  0   |       1       |  1   |
|  0   |       1       |  1   |       1       |  0   |       1       |  0   |
|  0   |       1       |  0   |       1       |  0   |       1       |  1   |
|  0   |       1       |  0   |       1       |  0   |       1       |  0   |

### 9&deg;

| ($\neg$ |  (p  | $\vee$ |  (q  | $\vee$ | r))) | $\leftrightarrow$ | ((p  | $\vee$ |  q)  | $\wedge$ |  (p  | $\vee$ | r))  |
| :-----: | :--: | :----: | :--: | :----: | :--: | :---------------: | :--: | :----: | :--: | :------: | :--: | :----: | :--: |
|    0    |  1   |   1    |  1   |   11   |  1   |         0         |  1   |   1    |  1   |    1     |  1   |   1    |  1   |
|    0    |  1   |   1    |  1   |   1    |  0   |         0         |  1   |   1    |  1   |    1     |  1   |   1    |  0   |
|    0    |  1   |   1    |  0   |   1    |  1   |         0         |  1   |   1    |  0   |    1     |  1   |   1    |  1   |
|    0    |  1   |   1    |  0   |   0    |  0   |         0         |  1   |   1    |  0   |    1     |  1   |   1    |  0   |
|    0    |  0   |   1    |  1   |   1    |  1   |         0         |  0   |   1    |  1   |    1     |  0   |   1    |  1   |
|    0    |  0   |   1    |  1   |   1    |  0   |         1         |  0   |   1    |  1   |    0     |  0   |   0    |  0   |
|    0    |  0   |   1    |  0   |   1    |  1   |         1         |  0   |   0    |  0   |    0     |  0   |   1    |  1   |
|    1    |  0   |   0    |  0   |   0    |  0   |         0         |  0   |   0    |  0   |    0     |  0   |   0    |  0   |

## 练习2

参照$P17$归纳定义不容易错写、漏写。

### 1.

$L_0 = X_1 = \{x_1 \}$

$L_1 = \{\neg\ x_1,\ x_1 \rightarrow x_1 \}$

$L_2 = \{\neg(\neg\ x_1),\ \neg(x_1 \rightarrow x_1),\ x_1 \rightarrow (\neg x_1),\ x_1 \rightarrow (x_1 \rightarrow x_1),\ (\neg x_1) \rightarrow x_1,\ (x_1 \rightarrow x_1) \rightarrow x_1 \}$

### 2.

$L_0 = X_2 = \{x_1,\ x_2\}$

$L_1 = \{\neg\ x_1,\ \neg\ x_2,\ x_1 \rightarrow x_1,\ x_1 \rightarrow x_2,\ x_2 \rightarrow x_1,\ x_2 \rightarrow x_2 \}$

$L_2 = \{\neg(\neg\ x_1),\ \neg(\neg\ x_2),\ \neg(x_1 \rightarrow x_1),\ \neg(x_1 \rightarrow x_2),\ \neg(x_2 \rightarrow x_1),\ \neg(x_2 \rightarrow x_2),\ \neg(x_1 \rightarrow x_1),\qquad\ \newline x_1 \rightarrow (\neg x_1),\ x_1 \rightarrow (\neg x_2),\ x_1 \rightarrow (x_1 \rightarrow x_1),\ x_1 \rightarrow (x_1 \rightarrow x_2),\ x_1 \rightarrow (x_2 \rightarrow x_1),\ x_1 \rightarrow (x_2 \rightarrow x_2),\newline x_2 \rightarrow (\neg x_1),\ x_2 \rightarrow (\neg x_2),\ x_2 \rightarrow (x_1 \rightarrow x_1),\ x_2 \rightarrow (x_1 \rightarrow x_2),\ x_2 \rightarrow (x_2 \rightarrow x_1),\ x_2 \rightarrow (x_2 \rightarrow x_2),\newline (\neg x_1)\rightarrow x_1,\ (\neg x_2)\rightarrow x_1,\ (x_1 \rightarrow x_1)\rightarrow x_1,\ (x_1 \rightarrow x_2)\rightarrow x_1,\ (x_2 \rightarrow x_1)\rightarrow x_1,\ (x_2 \rightarrow x_2)\rightarrow x_1,\newline (\neg x_1)\rightarrow x_2,\ (\neg x_2)\rightarrow x_2,\ (x_1 \rightarrow x_1)\rightarrow x_2,\ (x_1 \rightarrow x_2)\rightarrow x_2,\ (x_2 \rightarrow x_1)\rightarrow x_2,\ (x_2 \rightarrow x_2)\rightarrow x_2 \}$

### 3.

$|L_0| = |X_3| = 3$

$|L_1| = 3 + 3 \times 3 = 12$

$|L_2| = 12 + 3\times 12 + 12\times 3 = 84$

$|L_3| = 84 + 3 \times 84 + 84 \times 3 + 12 \times 12 = 732$

