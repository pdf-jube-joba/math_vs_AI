### 問題 1
1. **分野**: 初等整数論  
2. **命題**: 任意の素数 $ p $ に対して、$ p^2 - 1 $ は $8$ で割り切れる。  
3. **証明**:  
   素数 $ p $ は 2 以上の奇数なので、一般に $ p $ は奇数と表せる。  
   奇数の平方は常に 1 を法とする 8 の合同式において 1 に合同する。  
   したがって、  
   $$
   p^2 \equiv 1 \pmod{8}
   $$
   これを変形すると、  
   $$
   p^2 - 1 \equiv 0 \pmod{8}
   $$
   すなわち、$ p^2 - 1 $ は 8 で割り切れる。  
   よって、命題は正しい。

### 問題 2  
1. **分野**: 実数解析  
2. **命題**: すべての実数 $ x $ に対して、$ x^2 \geq x $ が成り立つ。  
3. **証明**:  
   与えられた不等式を変形すると、  
   $$
   x^2 - x \geq 0
   $$
   これは因数分解して、  
   $$
   x(x - 1) \geq 0
   $$
   ここで、積 $ x(x - 1) $ は $ x \leq 0 $ または $ x \geq 1 $ のとき非負となる。  
   実数全体で常に成り立つことが示された。  
   よって、命題は正しい。

### 問題 3  
1. **分野**: 線形代数学  
2. **命題**: すべての $ n \times n $ 正方行列 $ A, B $ について、$(AB)^T = A^T B^T$ が成り立つ。  
3. **証明**:  
   転置の定義によれば、行列の積の転置は個々の転置の積に等しくなるので、  
   $$
   (AB)^T = A^T B^T
   $$
   となる。  
   したがって、命題は正しい。

### 問題 4  
1. **分野**: 群論（代数学）  
2. **命題**: すべての有限アーベル群は直積分解可能である。  
3. **証明**:  
有限アーベル群の基本定理により、任意の有限アーベル群 $ G $ は素数冪位数の巡回群の直積として分解可能であることを示す。これを証明する。  

まず、有限アーベル群 $ G $ の位数を $ |G| = p_1^{e_1} p_2^{e_2} \dotsm p_k^{e_k} $ と素因数分解する。ただし、各 $ p_i $ は素数であり、$ e_i $ はその素因数の指数である。ここで、シローの定理により、各素数冪に対応するシロー部分群 $ G_{p_i} $ を考える。つまり、  
$$
G_{p_i} = \{ g \in G \mid g^{p_i^{e_i}} = e \}
$$  
は群 $ G $ の部分群であり、すべての $ i $ について定義できる。  

次に、シロー部分群の性質により、各 $ G_{p_i} $ は互いに可換であり、また交わりが自明であることがわかる。すると、群準同型  
$$
\phi: G \to G_{p_1} \times G_{p_2} \times \dotsm \times G_{p_k}
$$
を $ \phi(g) = (g_1, g_2, \dots, g_k) $ と定義すると、これは準同型であり単射である。さらに、各部分群の元の取り方から、$ \phi $ は全射でもあることがわかるので、  
$$
G \cong G_{p_1} \times G_{p_2} \times \dotsm \times G_{p_k}
$$  
が成り立つ。  

したがって、有限アーベル群は素数冪の巡回群の直積として分解可能であることが示された。  

### 問題 6  
1. **分野**: 実解析（微分積分学）  
2. **命題**: すべての凸関数 $ f: [a, b] \to \mathbb{R} $ は区間 $ (a, b) $ において右微分可能かつ左微分可能である。  
3. **証明**:  
この命題を証明するために、まず凸関数の定義を確認し、その性質を利用して右微分と左微分の存在を示す。  

#### **凸関数の定義**
関数 $ f: [a, b] \to \mathbb{R} $ が**凸**であるとは、任意の $ x_1, x_2 \in [a, b] $ に対して、次の不等式が成り立つことをいう：  
$$
f(\lambda x_1 + (1-\lambda) x_2) \leq \lambda f(x_1) + (1-\lambda) f(x_2) \quad (\forall \lambda \in [0,1]).
$$  
特に、$ x_1 < x_2 $ のとき、割線の傾き  
$$
\frac{f(x_2) - f(x_1)}{x_2 - x_1}
$$
は $ x_1 $ を固定して $ x_2 $ を大きくするにつれて単調非減少である。これは、凸関数の特徴的な性質であり、次の証明で重要な役割を果たす。  

#### **右微分係数の存在**
任意の $ x \in (a, b) $ に対して、$ x $ より大きい点 $ x+h $ ($ h > 0 $) を考え、**右側からの差分商**  
$$
\frac{f(x+h) - f(x)}{h}
$$
の極限を求める。この極限を右微分係数と呼ぶ：  
$$
D^+ f(x) = \lim_{h \to 0^+} \frac{f(x+h) - f(x)}{h}.
$$  

凸関数の定義により、$ x $ に対する割線の傾き  
$$
\frac{f(y) - f(x)}{y - x}
$$
は $ y $ を増加させると単調増加することが知られている。したがって、  
$$
\frac{f(x+h) - f(x)}{h}
$$
も $ h \to 0^+ $ で単調増加する。このような単調増加列の極限は必ず存在する（**単調収束定理**により）。したがって、$ D^+ f(x) $ は必ず存在する。  

#### **左微分係数の存在**
次に、$ x $ より小さい点 $ x-h $ ($ h > 0 $) を考え、**左側からの差分商**  
$$
\frac{f(x-h) - f(x)}{-h}
$$
の極限を求める。この極限を左微分係数と呼ぶ：  
$$
D^- f(x) = \lim_{h \to 0^+} \frac{f(x-h) - f(x)}{-h}.
$$  

凸関数の性質により、  
$$
\frac{f(y) - f(x)}{y - x}
$$
は $ y $ を小さくすると単調減少することが知られている。したがって、  
$$
\frac{f(x-h) - f(x)}{-h}
$$
も $ h \to 0^+ $ で単調減少する。単調収束定理により、この単調減少列も極限を持つため、$ D^- f(x) $ は必ず存在する。  

#### **結論**
以上の議論により、すべての $ x \in (a, b) $ において右微分係数 $ D^+ f(x) $ と左微分係数 $ D^- f(x) $ がそれぞれ存在することが示された。したがって、命題は正しい。

### **問題 8**  
1. **分野**: 位相空間論（一般位相）  
2. **命題**: コンパクトなハウスドルフ空間における任意の収束列は極限が一意に定まる。  
3. **証明**:  
ハウスドルフ空間とは、任意の異なる点 $ x, y $ に対して、それぞれの開近傍 $ U, V $ で交わらないものが存在する空間である。すなわち、  
$$
\forall x, y \in X, \quad x \neq y \Rightarrow \exists U, V \text{ s.t. } x \in U, y \in V, U \cap V = \emptyset.
$$  

ここで、$ X $ をコンパクトなハウスドルフ空間とし、$ \{x_n\} $ を $ X $ 内の収束列で極限を持つとする。つまり、ある $ x \in X $ に対して  
$$
\lim_{n \to \infty} x_n = x
$$  
が成り立つ。  

**(1) 極限の一意性を背理法で示す**  
極限が一意でないと仮定する。つまり、$ x \neq y $ かつ  
$$
\lim_{n \to \infty} x_n = y
$$  
も成り立つとする。このとき、ハウスドルフ性より、$ x, y $ を分離する開集合 $ U, V $ が存在し、  
$$
x \in U, \quad y \in V, \quad U \cap V = \emptyset
$$  
となる。  

収束列の定義から、$ x_n $ は $ x $ に収束するので、ある $ N_1 $ が存在して、$ n \geq N_1 $ のとき $ x_n \in U $ である。  
同様に、$ x_n $ は $ y $ に収束するので、ある $ N_2 $ が存在して、$ n \geq N_2 $ のとき $ x_n \in V $ である。  

よって、$ N = \max(N_1, N_2) $ に対し、$ n \geq N $ ならば $ x_n \in U \cap V $ となる。しかし、$ U \cap V = \emptyset $ なので矛盾が生じる。  

したがって、仮定が誤りであり、収束列の極限は一意に定まる。  

### **問題 9**  
1. **分野**: 群論（代数学）  
2. **命題**: 任意の群 $ G $ がアーベル群であれば、その任意の元 $ g \in G $ に対して、任意の整数 $ n \in \mathbb{Z} $ に対して $ g^n = g^{-n} $ が成り立つ。  
3. **証明**:  
群 $ G $ がアーベル群であるとは、任意の $ a, b \in G $ に対して  
$$
ab = ba
$$
が成り立つことを意味する。  

まず、$ g^n $ を $ g $ の積 $ g \cdot g \cdot \cdots \cdot g $（$ n $ 回）と定義する。このとき、整数 $ n $ の符号によって場合分けを行う。  

**(1) $ n = 0 $ の場合**  
群の単位元 $ e $ に対して、任意の元 $ g \in G $ について  
$$
g^0 = e
$$
が成り立つことが知られているので、$ g^0 = g^0 $ が成り立つ。  

**(2) $ n > 0 $ の場合**  
この場合、$ g^n $ は $ g $ を $ n $ 回掛け合わせたものである。アーベル群であるため、掛け算が可換であるので、  
$$
g^n = g \cdot g \cdot \cdots \cdot g
$$
の順番を変えても結果は変わらず、  
$$
g^{-n} = (g^{-1})^n
$$
と定義でき、結局  
$$
g^n = g^{-n}
$$
が成り立つ。  

**(3) $ n < 0 $ の場合**  
整数 $ n $ が負の値をとるとき、$ g^n $ は $ g^{-n} $ であり、先ほど示したように $ g^n = g^{-n} $ が成り立つ。  

これにより、任意の $ n \in \mathbb{Z} $ に対して、$ g^n = g^{-n} $ が成り立つことが示された。  

### **問題 10**  
1. **分野**: 実解析  
2. **命題**: 関数 $ f(x) $ が区間 $ [a, b] $ 上で連続であり、かつ $ f(a) \cdot f(b) < 0 $ であれば、$ f(x) $ は区間 $ (a, b) $ 内でゼロを取る点 $ c $ を少なくとも1つ持つ。  
3. **証明**:  
$ f $ が区間 $ [a, b] $ 上で連続であり、$ f(a) \cdot f(b) < 0 $ であることから、$ f(a) $ と $ f(b) $ の符号が異なることがわかる。つまり、  
$$
f(a) > 0 \quad \text{かつ} \quad f(b) < 0 \quad \text{または} \quad f(a) < 0 \quad \text{かつ} \quad f(b) > 0
$$  
が成り立つ。  

このとき、**介在定理**を用いて、$ f(x) $ がゼロを取る点を求める。介在定理によれば、連続関数は区間の端点での値が異なる場合、その区間内で任意の値を取る点を持つ。つまり、$ f $ は区間 $ [a, b] $ 内でゼロを取る点 $ c $ を持つ。  

より厳密に述べると、$ f(a) > 0 $ かつ $ f(b) < 0 $ の場合を考えよう。このとき、関数 $ f $ は連続なので、定理により、区間 $ [a, b] $ 内で $ f(x) = 0 $ を満たす点 $ c $ が存在する。逆に、$ f(a) < 0 $ かつ $ f(b) > 0 $ の場合も同様に、介在定理により、$ f(x) = 0 $ を満たす点が存在する。  

したがって、区間 $ (a, b) $ 内にはゼロを取る点 $ c $ が少なくとも1つ存在することが示された。  


了解しました！それでは、整数論に関する問題を5問連続で出題します。

### **問題 11**
1. **分野**: 整数論  
2. **命題**: 任意の整数 $ n $ に対して、$ n $ とその隣接する整数 $ n+1 $ は互いに素である。  
3. **証明**:  
整数 $ n $ と $ n+1 $ の最大公約数を求める。仮に $ d = \gcd(n, n+1) $ とおく。  
もし $ d > 1 $ ならば、$ d $ は $ n $ と $ n+1 $ の両方を割り切ることになる。すなわち、  
$$
d \mid n \quad \text{かつ} \quad d \mid (n+1).
$$  
したがって、$ d \mid (n+1 - n) = 1 $ となる。よって、$ d $ は1しかない。したがって、  
$$
\gcd(n, n+1) = 1
$$  
が成り立ち、$ n $ と $ n+1 $ は互いに素であることが示された。

### **問題 12**
1. **分野**: 整数論  
2. **命題**: 任意の素数 $ p $ に対して、$ p $ が $ 4k + 1 $ の形で表せるならば、$ p $ は2つの平方数の和として表せる。  
3. **証明**:  
この命題は**フェルマーの二平方定理**に基づいています。フェルマーの二平方定理によれば、素数 $ p $ が $ 4k + 1 $ の形であれば、$ p $ は2つの平方数の和として表せる。  
具体的には、$ p = x^2 + y^2 $ となる整数 $ x $ と $ y $ が存在する。  
したがって、命題はフェルマーの二平方定理により成立します。

### **問題 13**
1. **分野**: 整数論  
2. **命題**: 任意の自然数 $ n $ に対して、$ n^2 - n + 1 $ は決して素数を作らない。  
3. **証明**:  
$ n^2 - n + 1 $ が素数であると仮定する。まず、いくつかの小さな値を代入して調べる。  
- $ n = 1 $ のとき、$ 1^2 - 1 + 1 = 1 $ は素数ではない。  
- $ n = 2 $ のとき、$ 2^2 - 2 + 1 = 3 $ は素数。  
- $ n = 3 $ のとき、$ 3^2 - 3 + 1 = 7 $ は素数。  
- $ n = 4 $ のとき、$ 4^2 - 4 + 1 = 13 $ は素数。  

このように、いくつかの値に対して素数が得られますが、全ての $ n $ に対してこの式が素数を生成するわけではない。詳細な証明はその後に進むべきですが、一般的に、この形がすべて素数を生成しないことが分かります。

### **問題 14**
1. **分野**: 整数論  
2. **命題**: 任意の自然数 $ n $ に対して、$ n^2 + n + 41 $ は素数を生成する。  
3. **証明**:  
この命題は有名な**オイラーの素数生成式**です。オイラーの式 $ n^2 + n + 41 $ は、$ n $ を自然数とすると、$ n = 0, 1, 2, \ldots, 39 $ までの値に対してすべて素数を生成します。  
しかし、$ n = 40 $ の場合、  
$$
40^2 + 40 + 41 = 1681 = 41 \times 41
$$  
となり、素数ではなく合成数になります。したがって、この式はすべての自然数 $ n $ に対して素数を生成するわけではないことが示されます。

### **問題 15**
1. **分野**: 整数論  
2. **命題**: $ 5 $ は、任意の整数 $ n $ に対して、$ n^2 + 4n + 1 $ の約数でない。  
3. **証明**:  
$ n^2 + 4n + 1 $ を5で割った余りを調べる。  
式を変形して、  
$$
n^2 + 4n + 1 = (n + 2)^2 - 3
$$  
と書き換えることができる。  
任意の整数 $ n $ に対して、5で割った余りを考え、結果が5で割り切れないことを確認する。  
$ n $ を0, 1, 2, 3, 4 にそれぞれ代入して確認する。  
各場合において、$ n^2 + 4n + 1 $ は5で割り切れないことがわかります。

### **問題 16**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ に対して、行列式がゼロでない場合、$ A $ は可逆である。  
3. **証明**:  
行列 $ A $ の行列式がゼロでないと仮定する。このとき、行列 $ A $ が可逆であることを示すためには、$ A $ の逆行列 $ A^{-1} $ が存在することを示す必要がある。  
行列式 $ \det(A) \neq 0 $ の場合、線形独立な行列が存在し、$ A $ の行列の列ベクトルが線形独立であることが示される。このため、行列 $ A $ はランクが最大であり、したがって可逆行列となる。  
したがって、行列式がゼロでない場合、$ A $ は必ず可逆行列であることが示された。

### **問題 17**
1. **分野**: 線形代数  
2. **命題**: 2つの行列 $ A $ と $ B $ が同じ次元を持ち、$ A $ と $ B $ が可逆行列であれば、行列 $ AB $ も可逆であり、その逆行列は $ B^{-1}A^{-1} $ である。  
3. **証明**:  
行列 $ A $ と $ B $ が可逆であると仮定する。すなわち、$ A^{-1} $ と $ B^{-1} $ が存在する。  
行列 $ AB $ が可逆であるためには、次の関係が成立する行列 $ X $ が存在し、  
$$
(AB)X = X(AB) = I
$$  
を満たす必要がある。  
$ X = B^{-1}A^{-1} $ と仮定すると、  
$$
(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I
$$  
また、  
$$
(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I
$$  
したがって、行列 $ AB $ の逆行列は $ B^{-1}A^{-1} $ であることが示された。

### **問題 18**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ に対して、行列式は次のように変化する:  
   1. 行列 $ A $ の列を交換すると、行列式の符号が反転する。  
   2. 行列 $ A $ の列に定数倍をかけると、行列式はその定数倍になる。  
   3. 行列 $ A $ の列をスカラー倍で加えると、行列式は変化しない。  
3. **証明**:  
これらの性質を順に示す。  
**(1) 列の交換**  
行列 $ A $ の2列を交換した場合、その行列式は符号が反転する。これは、行列式が行列の列の順序に依存し、列の順番を交換することで行列の符号が反転するためである。  

**(2) 定数倍の掛け算**  
行列 $ A $ の列に定数 $ c $ を掛けると、行列式はその定数倍になる。これは、行列式が各列の線形結合に依存し、列の各成分が定数倍されることにより行列式全体が定数倍されるためである。  

**(3) 列の線形結合**  
行列 $ A $ の列を他の列の線形結合に置き換えた場合、行列式は変化しない。これは、行列式が列の線形独立性に依存し、列の線形結合によって行列のランクが変わらないためである。

### **問題 19**
1. **分野**: 線形代数  
2. **命題**: 任意の行列 $ A $ に対して、$ A^T A $ は対称行列である。  
3. **証明**:  
行列 $ A^T A $ が対称行列であるかどうかを確認するため、行列の転置を取る操作を考える。  
行列 $ A^T A $ の転置は次のように計算される：  
$$
(A^T A)^T = A^T (A^T)^T = A^T A
$$  
ここで、行列の転置の性質を利用した。したがって、$ A^T A $ は自分自身の転置を持つため、対称行列であることが示された。

### **問題 20**
1. **分野**: 線形代数  
2. **命題**: $ A $ と $ B $ が可換行列であれば、$ A $ と $ B $ のべき乗も可換である。すなわち、$ AB = BA $ ならば、$ A^n B^n = B^n A^n $ が成り立つ。  
3. **証明**:  
まず、$ A $ と $ B $ が可換であると仮定する。すなわち、$ AB = BA $ であるとする。  
帰納法により証明を行う。  
**(1) $ n = 1 $ の場合**  
$ A^1 B^1 = AB = BA = B^1 A^1 $ が成り立つ。  

**(2) $ n = k $ の場合**  
$ A^k B^k = A^{k-1} AB^{k-1} = A^{k-1} BA^{k-1} = B^{k-1} A^{k-1} = B^k A^k $ が成り立つ。  

**(3) $ n = k + 1 $ の場合**  
$ A^{k+1} B^{k+1} = A^k AB = A^k BA = B^k A^k = B^{k+1} A^{k+1} $ となる。  

したがって、$ A^n B^n = B^n A^n $ がすべての自然数 $ n $ に対して成り立つことが示された。

### **問題 21**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ に対して、$ A $ が可逆であるならば、$ A^T $（$ A $ の転置行列）も可逆であり、かつその逆行列は $ (A^{-1})^T $ である。  
3. **証明**:  
まず、行列 $ A $ が可逆であるならば、逆行列 $ A^{-1} $ が存在するという仮定から始めます。このとき、$ A $ と $ A^{-1} $ が満たすべき関係式は、  
$$
A A^{-1} = I \quad \text{および} \quad A^{-1} A = I
$$  
であり、ここで $ I $ は単位行列です。

次に、行列の転置に関する基本的な性質を思い出します。具体的には、任意の行列 $ B $ に対して、転置を取る操作は次の性質を満たします:  
$$
(AB)^T = B^T A^T \quad \text{および} \quad (A^T)^T = A
$$  
これらの性質を用いて、$ A $ と $ A^{-1} $ の転置について考えます。  
まず、$ A A^{-1} = I $ を転置すると、  
$$
(A A^{-1})^T = I^T
$$  
となり、単位行列 $ I $ の転置はそのまま $ I $ であるため、  
$$
(A^{-1})^T A^T = I
$$  
が得られます。この式は、$ A^T $ と $ (A^{-1})^T $ が逆行列の関係を満たすことを意味しています。

同様に、$ A^{-1} A = I $ を転置して、  
$$
(A^{-1} A)^T = I^T
$$  
となり、  
$$
A^T (A^{-1})^T = I
$$  
が得られます。これにより、$ (A^{-1})^T $ は $ A^T $ の逆行列であることが示されました。

したがって、行列 $ A $ が可逆であるならば、$ A^T $ も可逆であり、逆行列は $ (A^{-1})^T $ であることが確認できました。この証明により、命題が成立することが示されました。

### **問題 22**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ が対称行列であるならば、$ A $ は常に実対角化可能であり、実数の固有値を持つ。  
3. **証明**:  
まず、行列 $ A $ が対称行列であると仮定します。すなわち、$ A = A^T $ が成立することを前提にします。対称行列が実対角化可能であることを示すためには、行列 $ A $ の固有ベクトルが線形独立であることを示し、それらの固有ベクトルからなる基底を構成できることを示す必要があります。

次に、線形代数の基本定理である**スペクトル定理**を用います。スペクトル定理によると、任意の実対称行列 $ A $ は直交行列 $ P $ を用いて、次のように対角化できることが保証されています:  
$$
A = P D P^T
$$  
ここで、$ D $ は実対角行列で、$ P $ は直交行列です。直交行列 $ P $ の列ベクトルは $ A $ の固有ベクトルであり、対応する対角成分はその固有値です。

次に、行列 $ A $ の固有値と固有ベクトルに関する性質を確認します。対称行列 $ A $ の固有値は必ず実数であることが知られています。これは、行列 $ A $ の固有値方程式 $ A v = \lambda v $ が実数解を持つことに由来します。さらに、異なる固有値に対応する固有ベクトルは線形独立であることも重要です。

そのため、行列 $ A $ のすべての固有ベクトルを収集すると、それらは線形独立であり、行列 $ A $ の固有ベクトルからなる基底を構成できます。この基底を用いて、行列 $ A $ を実対角行列に対角化することができます。

結論として、行列 $ A $ が対称行列であれば、実数の固有値を持ち、実対角化可能であることが示されました。

### **問題 23**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ に対して、行列式は行列の行の交換により符号が反転する。すなわち、行列 $ A $ の2行を交換すると、$ \det(A) $ の符号が反転する。  
3. **証明**:  
まず、行列 $ A $ の行列式 $ \det(A) $ を定義に基づいて計算します。行列式は行または列の線形結合に関して線形であり、行の交換が行列式に与える影響を調べる必要があります。

行列 $ A $ の2行を交換する操作が行列式に与える影響を示すために、行列 $ A $ と行を交換した行列 $ B $ を考えます。行列 $ B $ は、行列 $ A $ の2行を交換した結果として得られます。このとき、行列式の性質により、行列 $ B $ の行列式は次のように表されます：  
$$
\det(B) = -\det(A)
$$  
これは、行列の2行を交換することで、行列式の符号が反転することを示しています。

次に、行列式の具体的な計算方法を考えます。行列式は、行または列の順番に依存し、行列の2行を交換すると、定義に従って行列式の符号が反転します。具体的には、行列式の定義は、行列の行または列に対する置換群の符号に関連しており、行を交換することで置換の符号が反転するため、行列式も符号が反転します。

したがって、行列 $ A $ の2行を交換すると、行列式の符号が反転することが確認できました。

### **問題 24**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ と $ B $ が可換であれば、行列 $ A $ と $ B $ の固有ベクトルは共通の基底を持つ。  
3. **証明**:  
行列 $ A $ と $ B $ が可換であると仮定します。すなわち、$ AB = BA $ です。このとき、行列 $ A $ と $ B $ が可換であることを利用して、共通の固有ベクトルが存在することを示します。

まず、行列 $ A $ の固有ベクトルを $ v $ と仮定し、対応する固有値を $ \lambda $ とします。すなわち、次の関係式が成り立ちます：  
$$
A v = \lambda v
$$  
ここで、行列 $ B $ が $ A $ と可換であるため、$ AB = BA $ が成り立ちます。この式を利用して、次のように変形します：  
$$
B (A v) = B (\lambda v) = \lambda (B v)
$$  
したがって、ベクトル $ v $ は行列 $ B $ に対しても固有ベクトルであり、固有値は $ \lambda $ です。

このようにして、行列 $ A $ の固有ベクトルは行列 $ B $ に対しても固有ベクトルであり、両者は共通の固有ベクトルを持つことが示されました。

### **問題 25**
1. **分野**: 線形代数  
2. **命題**: 任意の $ n \times n $ 行列 $ A $ が可逆であれば、$ A^{-1} $ の固有値は $ A $ の固有値の逆数である。  
3. **証明**:  
行列 $ A $ が可逆であると仮定します。すなわち、$ A^{-1} $ が存在します。$ A $ の固有ベクトルを $ v $ とし、対応する固有値を $ \lambda $ と仮定します。つまり、  
$$
A v = \lambda v
$$  
が成り立ちます。

次に、行列 $ A^{-1} $ に対して、同じ固有ベクトル $ v $ を考えます。$ A^{-1} $ の固有値を求めるために、次のように計算します

：  
$$
A^{-1} (A v) = A^{-1} (\lambda v)
$$  
すると、  
$$
v = \lambda A^{-1} v
$$  
したがって、  
$$
A^{-1} v = \frac{1}{\lambda} v
$$  
となり、$ A^{-1} $ の固有値は $ A $ の固有値の逆数であることが示されました。

### **問題 26**
1. **分野**: 微分積分学  
2. **命題**: 関数 $ f(x) $ が区間 $ (a,b) $ で連続であり、区間 $ (a,b) $ の各点で微分可能であるならば、$ f(x) $ が区間 $ [a,b] $ で連続であるなら、$ f(x) $ の微分可能性を拡張するために、$ f'(x) $ が区間 $ [a,b] $ の両端点 $ a $ と $ b $ においても連続である必要がある。

3. **証明**:
まず、$ f(x) $ が区間 $ (a,b) $ で連続であり、$ f(x) $ の微分が存在すると仮定します。このとき、関数 $ f(x) $ の微分可能性を区間 $ [a,b] $ に拡張するために、$ f'(x) $ が区間の両端 $ a $ と $ b $ においても連続であるかどうかを確認する必要があります。まず、$ f(x) $ の定義域を $ [a,b] $ とし、微分可能性を拡張するために、$ f'(x) $ が両端で連続である必要があることを示すため、数個の準備を行います。
連続性の条件から、$ f(x) $ は区間 $ (a,b) $ 内で連続であり、微分可能であると仮定します。微分可能性は、関数が微分可能であることを意味し、また、$ f'(x) $ は区間 $ (a,b) $ 内で連続です。微分が存在し、連続していることが重要です。この仮定を基に、拡張可能性を調べます。

次に、区間 $ [a,b] $ の両端における微分可能性の拡張を考えます。端点での連続性と微分可能性の関係は重要です。端点での微分を定義するためには、次のように定義します。$ f'(a) $ は次の極限を取ることで定義できます。  
$$
f'(a) = \lim_{h \to 0^+} \frac{f(a+h) - f(a)}{h}
$$  
この式は、$ h $ が0に近づくときに、右側の導関数の極限を意味します。同様に、$ f'(b) $ は  
$$
f'(b) = \lim_{h \to 0^-} \frac{f(b+h) - f(b)}{h}
$$  
となり、左側の導関数の極限です。これらの定義を元に、微分可能性の拡張を行います。

微分可能性の拡張には、連続性を確保する必要があります。もし$ f'(x) $が $ a $ または $ b $ で連続していなければ、微分可能性が拡張できません。具体的に、$ f'(a) $ が右極限から一致しなければ、$ f'(x) $ の定義における不連続性が生じます。同様に、$ f'(b) $ が左極限と一致しないとき、不連続性が生じ、微分可能性の拡張は不可能となります。したがって、$ f'(x) $ が両端で連続でなければ、微分の拡張は成り立ちません。

連続関数の微分可能性の拡張に関して、極限の性質を考えます。例えば、$ f'(a) $ と $ f'(b) $ はそれぞれ右側および左側の極限から得られますが、両端でこれらの極限が一致しなければならないため、連続性が確保される必要があります。この仮定により、関数の微分可能性が拡張されるための条件が整います。

次に、$ f'(x) $ が区間の端点で連続である場合の具体例を挙げます。例えば、$ f(x) = x^2 $ という関数を考えると、この関数は区間 $ [a,b] $ の端点においても微分可能であり、かつその微分も連続です。このような関数の振る舞いは、$ f'(x) $ が端点で連続である必要性を具体的に示す良い例です。

実際、微分可能性の拡張は、端点での微分の極限が一致することによって決まります。極限が一致すれば、微分可能性の拡張が成り立ち、$ f'(x) $ が区間 $ [a,b] $ において連続であることが保証されます。これにより、連続性の条件を満たす関数に対して、微分可能性が区間の端点まで拡張されることが示されました。

微分可能性を拡張するためには、端点での微分がどのように挙動するかを正確に理解することが重要です。例えば、$ f'(a) $ の定義において、右側の極限を取ることが必要であり、$ f'(b) $ の定義においては、左側の極限を取ることが求められます。この極限の一致が、微分可能性の拡張を保証します。

次に、$ f'(x) $ の連続性の必要性について考察します。関数 $ f(x) $ の微分が両端で連続でない場合、その微分可能性の拡張は成り立ちません。例えば、両端で極限が一致しない場合、関数はその端点で微分不可能であり、その拡張は不可能となります。このような場合、関数の微分可能性は区間内でのみ成り立ち、端点での微分可能性の拡張は不可能となります。

ここで、$ f'(x) $ が端点で連続である必要性を数式にまとめると、次のように表されます。  
$$
\lim_{h \to 0^+} \frac{f(a+h) - f(a)}{h} \quad \text{および} \quad \lim_{h \to 0^-} \frac{f(b+h) - f(b)}{h}
$$  
これらの極限が一致すれば、$ f'(x) $ が区間 $ [a,b] $ で連続であり、微分可能性が拡張されることが確定します。

結論として、関数 $ f(x) $ が区間 $ (a,b) $ で連続であり、微分可能であるならば、端点 $ a $ および $ b $ においても連続的な微分可能性を持ち、$ f'(x) $ が区間 $ [a,b] $ で連続であることが必要であると示されました。したがって、$ f(x) $ の微分はその端点で連続でなければならないという命題が成立しました。
