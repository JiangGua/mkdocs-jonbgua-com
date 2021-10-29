---
password: password
placeholder: 密码是 password
---



# LaTeX 公式

本文转自 https://www.cnblogs.com/nowgood/p/latexstart.html。



数学模式
----

在 LaTeX 中，最常用到的主要有文本模式和数学模式这两种模式。数学模式又可分为行内公式 {inline math) 和行间公式 (display math) 两种形式。

行内公式形式是将数学式插入文本行之内，使之与文本融为一体，这种形式适合编写简 短的数学式。

行间公式形式是将数学式插在文本行之间，自成一行或一个段落，与上下文附加一段垂 直空白，使数学式突出醒目。多行公式、公式组和微积分方程等复杂的数学式都是采用行间 公式形式编写。

行内公式 `$ ... $`

行间公式 `$$ ... $$`

```
函数 ${f(x)=a_nx^n+a_{n-1}x^{n-1}+a_{n-2}x^{n-2}}+\cdots$

函数 $${f(x)=a_nx^n+a_{n-1}x^{n-1}+a_{n-2}x^{n-2}}+\cdots \tag{1.1}$$
```

函数 ${f(x)=a_nx^n+a_{n-1}x^{n-1}+a_{n-2}x^{n-2}}+\cdots$

函数 

$$
{f(x)=a_nxn+a_{n-1}x{n-1}+a_{n-2}x^{n-2}}+\cdots \tag{1.1}
$$

> LaTeX 注释符号为 $\%$

### 输入上下标

`^` 表示上标, `_` 表示下标。如果上下标的内容多于一个字符，要用大括号 { } 把这些内容括起来当成一个整体。上下标是可以嵌套的，也可以同时使用。

$\sum_i^na_i$

```
$\sum_i^na_i$
```

### 输入分数

分数的输入形式为 `\frac{分子}{分母}`

$P(v)=\frac{1}{1+exp(-v/T)}$

```
$P(v)=\frac{1}{1+exp(-v/T)}$
```

### 上下划线与花括号

$$
\begin{array} \overline{a+b+c} \\ \underline{a+b+c} \\ \overleftarrow{a+b} \\ \underleftarrow{a+b} \\ \underleftrightarrow{a+b} \\ \vec x = \vec{AB} \\ \overbrace {a+b}^\text{a,b} \\ a+\rlap{\overbrace{\phantom{b+c+d}}^m}b+\underbrace{c+d+e}_n+f \end{array}
$$

```
$$
\begin{array}
\overline{a+b+c} \\
\underline{a+b+c} \\
\overleftarrow{a+b} \\
\underleftarrow{a+b} \\
\underleftrightarrow{a+b} \\
\vec x = \vec{AB} \\
\overbrace {a+b}^\text{a,b} \\
a+\rlap{\overbrace{\phantom{b+c+d}}^m}b+\underbrace{c+d+e}_n+f
\end{array}
$$
```

### 输入根号

$$
\begin{align*} \sqrt {12} \\ 
\sqrt[n]{12} 
\end{align*}
$$

```
$$
\begin{align*}
\sqrt {12} \\
\sqrt[n]{12} 
\end{align*}
$$
```

### 输入括号和分隔符

`(), [] , |` 分别表示原尺寸的形状，由于大括号 {} 在 LaTeX 中有特定含义, 所以使用需要转义, 即`\{` 和 `\}` 分别表示表示 { }。当需要显示大尺寸的上述符号时, 在上述符号前加上 `\left` 和 `\right` 命令.

$\{a\}$

$f(x,y,z) = 3y^2z 3+(\frac{7x+5}{1+y^2}) $$f(x,y,z) = 3y^2z + \left( 3 +\frac{7x+5}{1+y^2} \right)$

```
$\{a\}$
$f(x,y,z) = 3y^2z  3+(\frac{7x+5}{1+y^2}) $
$f(x,y,z) = 3y^2z + \left( 3 +\frac{7x+5}{1+y^2} \right)$
```

关于各种数学符号写法, 详见 [Cmd Markdown 公式指导手册](https://www.zybuluo.com/codeep/note/163962#cmd-markdown-%E5%85%AC%E5%BC%8F%E6%8C%87%E5%AF%BC%E6%89%8B%E5%86%8C), 下面主要介绍下常用的 矩阵和多行公式输入 做详细的记录.

矩阵
--

矩阵中, 不同的列使用 `&` 分割, 行使用 `\\` 分隔

下面展示一系列矩阵环境排版, 区别在于外面的括号不同

$$
\begin{align*} &\text{matrix}\quad\begin{matrix} a&b \\ c&d \end{matrix} \quad &\text{bmatrix}\quad\begin{bmatrix} a&b \\ c&d \end{bmatrix} \quad &\text{vmatrix}\quad\begin{vmatrix} a&b \\ c&d \end{vmatrix} \quad \\ &\text{pmatrix}\quad\begin{pmatrix} a&b \\ c&d \end{pmatrix} \quad &\text{Bmatrix}\quad\begin{Bmatrix} a&b \\ c&d \end{Bmatrix} \quad &\text{Vmatrix}\quad\begin{Vmatrix} a&b \\ c&d \end{Vmatrix} \quad\\ \end{align*}
$$

$$
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i 
\end{pmatrix} 
$$

$$
\chi(\lambda) =  
\begin{vmatrix}
\lambda - a & -b & -c \\
-d & \lambda - e & -f \\
-g & -h & \lambda - i 
\end{vmatrix}
$$

```
$$
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i 
\end{pmatrix} 
$$

$$
\chi(\lambda) =  
\begin{vmatrix}
\lambda - a & -b & -c \\
-d & \lambda - e & -f \\
-g & -h & \lambda - i 
\end{vmatrix}
$$
```

### 省略号

$$
\begin{eqnarray*} \\
\ldots \\
\cdots \\
\vdots \\
\ddots \\
\end{eqnarray*}
$$

```
$$
\begin{eqnarray*} \\
\ldots \\
\cdots \\
\vdots \\
\ddots \\
\end{eqnarray*}
$$
```

单行公式与多行公式
---------

`equation` 环境用来输入单行公式, 自动生成编号, 也可以使用 \tag{...} 自己对公式编号; 使用 `equation*` 环境, 不会自动生成公式编号, 后续介绍的公式输入环境都是在自动编号后面加上 `*` 便是不自动编号环境.

\begin{equation}
(a+b) \times c = a\times c + b \times c \\
\end{equation}

\begin{equation*}
(a+b) \times c = a\times c + b \times c \\
\end{equation*}

```
\begin{equation}
(a+b) \times c = a\times c + b \times c \\
\end{equation}
```

`\[ ... \]` 是 `equation*` 环境的简写

  

$$
(a+b) \times c = a\times c + b \times c \
$$

```
\\[
(a+b) \times c = a\times c + b \times c \\
\\]
```

`eqnarray` 环境用来输入按照等号 (或者其他关系符) 对齐的方程组, 编号

$$
\begin{eqnarray} f(x) = a_nx^n \\ g(x) = x^2 \end{eqnarray}
$$

```
$$
\begin{eqnarray}
f(x) = a_nx^n \\
g(x) = x^2
\end{eqnarray}
$$
```

输入多行公式, `gather` 环境得到的公式是每行居中的, `align`环境则允许公式按照等号或者其他关系符对齐, 在关系符前加`&`表示对齐

$$
\begin{gather} (a+b) \times c = a\times c + b \times c \notag \\ ac= a\times c \\ \end{gather}
$$

$$
\begin{align} y &= \cos t + 1 \\ y &= 2sin t \\ \end{align}
$$

```
$$
\begin{gather}
(a+b) \times c = a\times c + b \times c \notag \\
ac= a\times c \\
\end{gather}
$$

$$
\begin{align}
y &= \cos t + 1 \\
y &= 2sin t \\
\end{align}
$$
```

`align` 环境还允许排列多列对齐公式, 列与列之间使用`&`分割

$$
\begin{align*} x &= t & x &= \cos t & x &= t \\ y &= 2t & y &= \sin (t+1) & y &= \sin t \\ \end{align*}
$$

$$
\begin{align*} & (a+b)(a^2-ab+b^2) \\ = {}& a^3-a^2b+ab^2+a^2b-ab^2+b^2 \\ = {}& a^3 + b^3 \end{align*}
$$

```
$$
\begin{align*}
 x &= t & x &= \cos t &  x &= t \\
 y &= 2t & y &= \sin (t+1) & y &= \sin t \\
\end{align*}
$$

$$
\begin{align*}
& (a+b)(a^2-ab+b^2) \\
= {}& a^3-a^2b+ab^2+a^2b-ab^2+b^2 \\
= {}& a^3 + b^3
\end{align*}
$$
```

align 环境中列分隔符 & 一般放在关系符前面, 如果个别需要再关系符后面或者别的地方对齐的, 则应该注意使用的符号类型

$$
% 关系符后对齐，需要使用空的分组
% 代替关系符右侧符号，保证间距
\begin{align*} & (a+b)(a^2-ab+b^2) \notag \\ ={ } & a^3 - a^2b + ab^2 + a^2b - ab^2 + b^2 \notag \\ ={ } & a^3 + b^3 \label{eq:cubesum} \end{align*}
$$

```
$$
% 关系符后对齐，需要使用空的分组
% 代替关系符右侧符号，保证间距
\begin{align*}
    & (a+b)(a^2-ab+b^2) \notag \\
={ } & a^3 - a^2b + ab^2 + a^2b
      - ab^2 + b^2 \notag \\
={ } & a^3 + b^3 \label{eq:cubesum}
\end{align*}
$$
```

### 跨多行的单个公式

单个公式很长的时候需要换行，但仅允许生成一个编号时，可以用 split 环境包围公式代码，在需要转行的地方使用 \. split 环境一般用在 equation, gather 环境里面, 可以把单个公式拆成多行, 同时支持 align 那样对齐公式.

split 环境不产生编号, 编号由外面的数学环境产生; 每行需要使用 1 个 & 来标识对齐的位置，结束后可使用 \tag{...} 标签编号。 如果 split 环境中某一行不是在二元关系符前面对齐, 需要通过 \quad 等手段设置间距或对齐方式.

$$% 注意 \tag{...} 编号的位置 \begin{equation} \begin{split} \cos 2x &= \cos^2 x - \sin^2 x \\ &= 2\cos^2 x - 1 \end{split} \tag{3.1} \end{equation}$$

 

$$
\begin{equation}\label{eq:trigonometric} \begin{split} \frac12 (\sin(x+y) + \sin(x-y)) &= \frac12(\sin x\cos y + \cos x\sin y) \\ & \quad + \frac12(\sin x\cos y - \cos x\sin y) \\ &= \sin x\cos y \end{split} \end{equation}
$$

```
$$
% 注意 \tag{...} 编号的位置
\begin{equation}
\begin{split}
\cos 2x &= \cos^2 x - \sin^2 x \\
        &= 2\cos^2 x - 1  
\end{split} \tag{3.1}
\end{equation}  
$$

$$
\begin{equation}\label{eq:trigonometric}
\begin{split}
\frac12 (\sin(x+y) + \sin(x-y))
  &= \frac12(\sin x\cos y + \cos x\sin y) \\
  & \quad + \frac12(\sin x\cos y - \cos x\sin y) \\
  &= \sin x\cos y
\end{split}
\end{equation}
$$
```

### 将公式组合为块

最常见的是 `case 环境`, 他在几行公式前面用花括号括起来, 表示几种不同的情况; 每行公式使用 & 分隔, 便是表达式与条件, 例如

$$
\begin{equation} D(x) = \begin{cases} 1, & \text{if } x \in \mathbb{Q}; \\ 0, & \text{if } x \in \mathbb{R}\setminus\mathbb{Q}. \end{cases} \end{equation}
$$

```
$$
\begin{equation}
D(x) = \begin{cases}
1, & \text{if } x \in \mathbb{Q}; \\
0, & \text{if } x \in
     \mathbb{R}\setminus\mathbb{Q}.
\end{cases}
\end{equation}
$$
```

`gathered环境` 将几行公式居中排列, 组合为一个整体;

$$
\left. \begin{gathered} S \subseteq T \\ S \supseteq T \end{gathered} \right\} \implies S = T
$$

```
$$
\left. \begin{gathered}
S \subseteq T \\
S \supseteq T
\end{gathered} \right\}
\implies S = T  
$$
```

括号的其他用法
-------

<table><thead><tr><th>功能</th><th>语法</th><th>显示</th></tr></thead><tbody><tr><td>圆括号，小括号</td><td>\left(\frac{a}{b} \right)</td><td><span class="MathJax" id="MathJax-Element-31-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>(</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>)</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">(ab)</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>(</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>)</mo></mrow></math><script type="math/tex" id="MathJax-Element-31">\left( \frac{a}{b} \right)</script></span></td></tr><tr><td>方括号，中括号</td><td>\left[\frac{a}{b} \right]</td><td><span class="MathJax" id="MathJax-Element-32-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>[</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>]</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">[ab]</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>[</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>]</mo></mrow></math><script type="math/tex" id="MathJax-Element-32">\left[ \frac{a}{b} \right]</script></span></td></tr><tr><td>花括号，大括号</td><td>\left\{\frac{a}{b} \right\}</td><td><span class="MathJax" id="MathJax-Element-33-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>{</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>}</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">{ab}</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>{</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>}</mo></mrow></math><script type="math/tex" id="MathJax-Element-33">\left\{ \frac{a}{b} \right \}</script></span></td></tr><tr><td>尖括号</td><td>\left \langle \frac{a}{b} \right \rangle</td><td><span class="MathJax" id="MathJax-Element-34-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>&amp;#x27E8;</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>&amp;#x27E9;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">⟨ab⟩</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>⟨</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>⟩</mo></mrow></math><script type="math/tex" id="MathJax-Element-34">\left \langle \frac{a}{b} \right \rangle</script></span></td></tr><tr><td>单竖线，绝对值</td><td>\left | \frac{a}{b} \right|</td><td>丨<span class="MathJax" id="MathJax-Element-35-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mfrac><mi>a</mi><mi>b</mi></mfrac></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true"> ab</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mfrac><mi>a</mi><mi>b</mi></mfrac></math><script type="math/tex" id="MathJax-Element-35">\frac{a}{b}</script>丨</span></td></tr><tr><td>双竖线，范式</td><td>\left \| \frac{a}{b} \right \|</td><td><span class="MathJax" id="MathJax-Element-36-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo symmetric=&quot;true&quot;>&amp;#x2016;</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo symmetric=&quot;true&quot;>&amp;#x2016;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">∥∥ab∥∥</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo symmetric="true">‖</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo symmetric="true">‖</mo></mrow></math><script type="math/tex" id="MathJax-Element-36">\left \| \frac{a}{b} \right \|</script></span></td></tr><tr><td>取整函数</td><td>\left \lfloor \frac{a}{b} \right \rfloor</td><td><span class="MathJax" id="MathJax-Element-37-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>&amp;#x230A;</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>&amp;#x230B;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">⌊ab⌋</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>⌊</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>⌋</mo></mrow></math><script type="math/tex" id="MathJax-Element-37">\left \lfloor \frac{a}{b} \right \rfloor</script></span></td></tr><tr><td>取顶函数</td><td>\left \lceil \frac{c}{d} \right \rceil</td><td><span class="MathJax" id="MathJax-Element-38-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>&amp;#x2308;</mo><mfrac><mi>c</mi><mi>d</mi></mfrac><mo>&amp;#x2309;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">⌈cd⌉</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>⌈</mo><mfrac><mi>c</mi><mi>d</mi></mfrac><mo>⌉</mo></mrow></math><script type="math/tex" id="MathJax-Element-38">\left \lceil \frac{c}{d} \right \rceil</script></span></td></tr><tr><td>斜线与反斜线</td><td>\left / \frac{a}{b} \right \backslash</td><td><span class="MathJax" id="MathJax-Element-39-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo fence=&quot;true&quot; stretchy=&quot;true&quot; symmetric=&quot;true&quot;>/</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence=&quot;true&quot; stretchy=&quot;true&quot; symmetric=&quot;true&quot;>\</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">/ab\</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo fence="true" stretchy="true" symmetric="true">/</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence="true" stretchy="true" symmetric="true">\</mo></mrow></math><script type="math/tex" id="MathJax-Element-39">\left / \frac{a}{b} \right \backslash</script></span></td></tr><tr><td>上下箭头</td><td>\left \uparrow \frac{a}{b} \right \downarrow</td><td><span class="MathJax" id="MathJax-Element-40-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo fence=&quot;true&quot; symmetric=&quot;true&quot;>&amp;#x2191;</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence=&quot;true&quot; symmetric=&quot;true&quot;>&amp;#x2193;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">↑⏐⏐ab⏐↓⏐</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo fence="true" symmetric="true">↑</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence="true" symmetric="true">↓</mo></mrow></math><script type="math/tex" id="MathJax-Element-40">\left \uparrow \frac{a}{b} \right \downarrow</script></span></td></tr><tr><td>混合括号 1</td><td>\left [0,1 \right)</td><td><span class="MathJax" id="MathJax-Element-41-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>[</mo><mn>0</mn><mo>,</mo><mn>1</mn><mo>)</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">[0,1)</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>[</mo><mn>0</mn><mo>,</mo><mn>1</mn><mo>)</mo></mrow></math><script type="math/tex" id="MathJax-Element-41">\left [ 0,1 \right )</script></span></td></tr><tr><td>混合括号 2</td><td>\left \langle \psi \right\|</td><td><span class="MathJax" id="MathJax-Element-42-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>&amp;#x27E8;</mo><mi>&amp;#x03C8;</mi><mo symmetric=&quot;true&quot;>&amp;#x2016;</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">⟨ψ∥</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>⟨</mo><mi>ψ</mi><mo symmetric="true">‖</mo></mrow></math><script type="math/tex" id="MathJax-Element-42">\left \langle \psi \right \|</script></span></td></tr><tr><td>单左括号</td><td>\left \{\frac{a}{b} \right .</td><td><span class="MathJax" id="MathJax-Element-43-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo>{</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence=&quot;true&quot; stretchy=&quot;true&quot; symmetric=&quot;true&quot;></mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">{ab</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo>{</mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo fence="true" stretchy="true" symmetric="true"></mo></mrow></math><script type="math/tex" id="MathJax-Element-43">\left \{ \frac{a}{b} \right .</script></span></td></tr><tr><td>单右括号</td><td>\left . \frac{a}{b} \right \}</td><td><span class="MathJax" id="MathJax-Element-44-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mrow><mo fence=&quot;true&quot; stretchy=&quot;true&quot; symmetric=&quot;true&quot;></mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>}</mo></mrow></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">ab}</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mrow><mo fence="true" stretchy="true" symmetric="true"></mo><mfrac><mi>a</mi><mi>b</mi></mfrac><mo>}</mo></mrow></math><script type="math/tex" id="MathJax-Element-44">\left . \frac{a}{b} \right \}</script></span></td></tr></tbody></table>

希腊字母
----

<table><thead><tr><th>希腊字母 (小写)</th><th>输入</th><th>希腊字母 (大写)</th><th>输入</th></tr></thead><tbody><tr><td>α</td><td>\alpha</td><td>Α</td><td>A</td></tr><tr><td>β</td><td>\beta</td><td>Β</td><td>B</td></tr><tr><td>γ</td><td>\gamma</td><td>Γ</td><td>\Gamma</td></tr><tr><td>δ</td><td>\delta</td><td>Δ</td><td>\Delta</td></tr><tr><td>ε或ϵ</td><td>\epsilon 或 \ varepsilon</td><td>Ε</td><td>E</td></tr><tr><td>ζ</td><td>\zeta</td><td>Ζ</td><td>Z</td></tr><tr><td>η</td><td>\eta</td><td>Η</td><td>H</td></tr><tr><td>θ或ϑ</td><td>\theta 或 \ vartheta</td><td>Θ</td><td>\Theta</td></tr><tr><td>ι</td><td>\iota</td><td>Ι</td><td>I</td></tr><tr><td>κ</td><td>\kappa</td><td>Κ</td><td>K</td></tr><tr><td>λ</td><td>\lambda</td><td>Λ</td><td>\Lambda</td></tr><tr><td>μ</td><td>\mu</td><td>Μ</td><td>M</td></tr><tr><td>ν</td><td>\nu</td><td>Ν</td><td>N</td></tr><tr><td>ξ</td><td>\xi</td><td>Ξ</td><td>\Xi</td></tr><tr><td>ο</td><td>o</td><td>Ο</td><td>O</td></tr><tr><td>π或ϖ</td><td>\pi 或 \ varpi</td><td>Π</td><td>\Pi</td></tr><tr><td>ρ或ϱ</td><td>\rho 或 \ varrho</td><td>Ρ</td><td>P</td></tr><tr><td>σ或ς</td><td>\sigma 或 \ varsigma</td><td>Σ</td><td>\Sigma</td></tr><tr><td>τ</td><td>\tau</td><td>Τ</td><td>T</td></tr><tr><td>υ</td><td>\upsilon</td><td>Υ</td><td>\Upsilon</td></tr><tr><td>φ或φ</td><td>\phi 或 \ varphi</td><td>Φ</td><td>\Phi</td></tr><tr><td>χ</td><td>\chi</td><td>Χ</td><td>X</td></tr><tr><td>ψ</td><td>\psi</td><td>Ψ</td><td>\Psi</td></tr><tr><td>ω</td><td>\omega</td><td>Ω</td><td>\Omega</td></tr></tbody></table>

三角函数与逻辑数学字符
-----------

<table><thead><tr><th>数学字符</th><th>输入</th><th>数学字符</th><th>输入</th></tr></thead><tbody><tr><td>±</td><td>\pm</td><td>×</td><td>\times</td></tr><tr><td>÷</td><td>\div</td><td>|</td><td>\mid</td></tr><tr><td><span class="MathJax" id="MathJax-Element-45-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mo>&amp;#x2224;</mo></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true">∤</nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mo>∤</mo></math><script type="math/tex" id="MathJax-Element-45">\nmid</script></span></td><td>\nmid</td><td>⋅</td><td>\cdot</td></tr><tr><td>∘</td><td>\circ</td><td>∗</td><td>\ast</td></tr><tr><td>⨀</td><td>\bigodot</td><td>⨂</td><td>\bigotimes</td></tr><tr><td>⨁</td><td>\bigoplus</td><td>≤</td><td>\leq</td></tr><tr><td>≥</td><td>\geq</td><td>≠</td><td>\neq</td></tr><tr><td>≈</td><td>\approx</td><td>≡</td><td>\equiv</td></tr><tr><td>∑</td><td>\sum</td><td>∏</td><td>\prod</td></tr><tr><td>∐</td><td>\coprod</td><td>∅</td><td>\emptyset</td></tr><tr><td>∈</td><td>\in</td><td>∉</td><td>\notin</td></tr><tr><td>⊂</td><td>\subset</td><td>⊃</td><td>\supset</td></tr><tr><td>⊆</td><td>\subseteq</td><td>⊇</td><td>\supseteq</td></tr><tr><td>⋂</td><td>\bigcap</td><td>⋃</td><td>\bigcup</td></tr><tr><td>⋁</td><td>\bigvee</td><td>⋀</td><td>\bigwedge</td></tr><tr><td>⨄</td><td>\biguplus</td><td>⨆</td><td>\bigsqcup</td></tr><tr><td>log</td><td>\log</td><td>lg</td><td>\lg</td></tr><tr><td>ln</td><td>\ln</td><td>⊥</td><td>\bot</td></tr><tr><td>∠</td><td>\angle</td><td>30^∘</td><td>30 ^ \circ</td></tr><tr><td>sin</td><td>\sin</td><td>cos</td><td>\cos</td></tr><tr><td>tan</td><td>\tan</td><td>cot</td><td>\cot</td></tr><tr><td>′</td><td>\prime</td><td>∫</td><td>\int</td></tr><tr><td>∬</td><td>\iint</td><td>∭</td><td>\iiint</td></tr><tr><td>⨌</td><td>\iiiint</td><td>∮</td><td>\oint</td></tr><tr><td>lim</td><td>\lim</td><td>∞</td><td>\infty</td></tr><tr><td>∇</td><td>\nabla</td><td>∵</td><td>\because</td></tr><tr><td>∴</td><td>\therefore</td><td>∀</td><td>\forall</td></tr><tr><td>∃</td><td>\exists</td><td>≠</td><td>\not=</td></tr><tr><td>≯</td><td>\not&gt;</td><td>⊄</td><td>\not\subset</td></tr><tr><td>ŷ</td><td>\hat{y}</td><td>yˇ</td><td>\check{y}</td></tr><tr><td>y˘</td><td>\breve{y}</td><td>sec</td><td>\sec</td></tr><tr><td>↑</td><td>\uparrow</td><td>↓</td><td>\downarrow</td></tr><tr><td>⇑</td><td>\Uparrow</td><td>⇓</td><td>\Downarrow</td></tr><tr><td>→</td><td>\rightarrow</td><td>←</td><td>\leftarrow</td></tr><tr><td>⇒</td><td>\Rightarrow</td><td>⇐</td><td>\Leftarrow</td></tr><tr><td>⟶</td><td>\longrightarrow</td><td>⟵</td><td>\longleftarrow</td></tr><tr><td>⟹</td><td>\Longrightarrow</td><td>⟸</td><td>\Longleftarrow</td></tr><tr><td><span class="MathJax" id="MathJax-Element-46-Frame" tabindex="0" data-mathml="<math xmlns=&quot;http://www.w3.org/1998/Math/MathML&quot;><mspace width=&quot;1em&quot; ></mspace></math>" role="presentation" style="position: relative;"><nobr aria-hidden="true"></nobr><math xmlns="http://www.w3.org/1998/Math/MathML"><mspace width="1em"></mspace></math><script type="math/tex" id="MathJax-Element-46">\quad</script></span></td><td>\quad</td><td>#</td><td>#</td></tr></tbody></table>