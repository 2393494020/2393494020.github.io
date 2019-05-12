#### 函数

定义域（集合，与是否为实数无关）  
对应域（集合，与是否为实数无关）  
对应法则

### Limit

$$f(x) = x^2$$
$$\lim_{x \to 2}f(x)=L$$

极限式子描述的是一种永不停止的变化现象，不是一个数字或结果  
如上式子表示，当 x 无限逼近 2（但永远不会等于 2）的时候，f(x) 无限逼近 L

用图形探索极限的性质
1. 当x趋（逼）近c时与该点有无定义无关
2. 极限是一个定值
3. 讨论极限请先讨论其是否存在
4. 极限存在条件：左极限=右极限

#### 数学建模

学习探索解决问题的方法。  
问题：如何不透过画图求极限？  
$$\lim_{x \to c}f(x)=L$$
step1. 趋近 = 逼近 = 要多靠近有多靠近  
step2. 考虑两个靠近  
step3. 用 $\epsilon$ 表示在 y 轴上函数值 $f(x)$ 与 L 的靠近，数学上表示为 $|f(x) - L| < \epsilon$  
step4. 用 $\delta$ 表示 x 轴上自变数 x 与 c 的靠近，数学上表示为 $0 < |x - c| < \delta$  

step3 与 step4 有什么关系？（先后关系，对应关系）  
答：对每一个 $\epsilon$ 的靠近皆有 $\delta$ 的靠近来完成 

#### Definition

We say that
$$\lim_{x \to c}f(x)=L$$
if $\quad\forall\quad\epsilon>0, \quad\exists\quad\delta>0, \quad such\ that\quad\forall\ x\ in\ 0<|x-c|<\delta, \quad |f(x) - L|<\epsilon$

We say that
$$\lim_{x \to c^+}f(x)=L$$
if $\quad\forall\quad\epsilon>0, \quad\exists\quad\delta>0, \quad such\ that\quad\forall\ x\ in\ (c,\ c+\delta), \quad |f(x) - L|<\epsilon$


We say that
$$\lim_{x \to c^-}f(x)=L$$
if $\quad\forall\quad\epsilon>0, \quad\exists\quad\delta>0, \quad such\ that\quad\forall\ x\ in\ (c-\delta,\ c), \quad |f(x) - L|<\epsilon$

- Remark
  
  1.为什么先给 $\epsilon>0$，而后才有 $\exists>0$
  
  答:

  如果先给定$\delta>0$，则给定了自变数 $x$ 的范围$(c-\delta,\ c+\delta)$，其值域就决定了，从而没有所谓$f(x)$与L靠近不靠近的问题

  2.当 $\epsilon$ 变小时，$\delta$ 也变小，（因为 $f(x)$ 不断靠近 L，需要 $x$ 不断靠近 c 来完成），换言之，$\delta$ 由 $\epsilon$ 决定

  3.给定 $\epsilon>0$，$\exists\ \delta>0$，$\delta$ 不唯一（比如可以取任意比 $\delta$ 小的任意值）

  4.$\exists\ \delta>0$ 可以有两种情况，一种是寻找 $\delta>0$（即需要证明极限），另一种是得到 $\delta>0$（即已给定极限）

- show that

$$\lim_{x \to 3}2x=6$$

proof.

let $\epsilon>0$，

推演过程:  
$|2x-6|<\epsilon \ =>\ |x-3|<\frac{\epsilon}{2}$


take $\delta=\frac{\epsilon}{2}$，Then $\forall\ x\ in\ 0<|x-3|<\delta,\ |2x-6|<\epsilon$

Thearefore,
$$\lim_{x \to 3}2x=6$$

### Continuity

