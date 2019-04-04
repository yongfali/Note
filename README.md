# MarkDown Basic Grammer

# 标题
### Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。
类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）
任何数量的 = 和 - 都可以有效果

类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

# 2、区块引用 Blockquotes
Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。如果你还熟悉在 email 信件中的引言部分，你就知道怎么在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > 样例如下：
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 > 如下：

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：
> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     return shell_exec("echo $input | $markdown_script");

# 列表
Markdown 支持有序列表和无序列表。
>
无序列表使用星号、加号或是减号作为列表标记：
> 
>  * Red
>  * Green
>  * Blue

等同于：
> + Red
> + Green
> + Blue

也等同于：
> - Red
> - Green
> - Blue

有序列表则使用数字接着一个英文句点：
> 1. Red
> 2. Green
> 3. Blue

Markdown有序列表你可以完全不用在意数字的正确性，它会根据第一个数字自增序号，因此你只需要关注第一个起始的数字即可。如下的案例：
> 1. Red
> 1. Green
> 1. Blue

如果要在列表项目内放进引用，那 > 就需要缩进：

*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.
    
# 分隔线

你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

* * *
***
*****
- - -
---------------------------------------

# 区段元素

## 链接

Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
不管是哪一种，链接文字都是用 [方括号] 来标记。
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：

> This is [an example](http://example.com/ "Title") inline link.

> [This link](http://example.net/) has no title attribute.

> Use the `printf()` function.

参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

> This is [an example] [id] reference-style link.

接着，在文件的任意处，你可以把这个标记的链接内容定义出来：

\[id]：http://example.com/  "Optional Title Here"
> [id]: http://example.com/  "Optional Title Here"

# 强调

Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 \<em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 \<strong>，例如：

> *single asterisks*

> _single underscores_

> **double asterisks**

> __double underscores__
  
# 代码
如果要标记一小段行内代码，你可以用反引号把它包起来（`），例如：

> Use the `printf()` function.

如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段：

> ``There is a literal backtick (`) here.``

# 图片
很明显地，要在纯文字应用中设计一个「自然」的语法来插入图片是有一定难度的。Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。

行内式的图片语法看起来像是：
> ![Alt text](/path/to/img.jpg)

> ![Alt text](/path/to/img.jpg "Optional title")

详细叙述如下：
> + 一个惊叹号 !
> +    接着一个方括号，里面放上图片的替代文字
> +    接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 
> +    选择性的 'title' 文字。

参考式的图片语法则长得像这样：

![Alt text][id]

「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

> [id]: url/to/image  "Optional title attribute"

到目前为止， Markdown还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 \<img> 标签。


# 其它
### 自动链接
Markdown 支持以比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来， Markdown 就会自动把它转成链接。一般网址的链接文字就和链接地址一样，例如：

> <http://example.com/>

# 首段空格
\&nbsp;//半角空格（英文）

\&emsp;//全角空格（中文）

&emsp;&emsp;参考式的链接是在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记：

# Table制作

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |



# Markdown Common Mathematical Formulas

## 常用数学公式和符号表示
### 1. 上下标
<font size="4">

^表示上标，_表示下标，如果上（下）标内容多于一个字符就需要使用{}，注意不是( ), 因为( )经常是公式本身组成部分，为避免冲突，所以选用了{ } 将其包起来。

**示例：**
> $x^{y^z}=(1+e^x)^{-2xy^w}$

**效果：**

```math
 x^{y^z}=(1+e^x)^{-2xy^w}
```

上面输入的上下标都是在字符的右侧，要想在左侧或者两侧都写上下标，那么需要使用\sideset语法。

**示例：**
> $\sideset{^1_2}{^3_4}\bigotimes$

</font>

### 2. 括号和分隔符
<font size="4">
( )和[ ]就是自身了，由于{ } 是Tex的元字符，所以表示它自身时需要转义。

**示例：**
> $f(x,y) = x^2 + y^2, x\epsilon[0,100]$

**效果：**

```math
 f(x,y) = x^2 + y^2, x\epsilon[0,100]
```

有时候括号需要大号的，普通括号不好看，此时需要使用\left和\right加大括号的大小。

**示例：**
> $(\frac{x}{y})^8$，$\left(\frac{x}{y}\right)^8$

</font>

### 3. 分数、开方、省略号
<font size="4">
使用\frac{分子}{分母}格式，或者 分子\over 分母。

**示例：**
> $\frac{1}{2x+1}$或者$1\over{2x+1}$

**效果：**

```math
 1\over{2x+1}
```

开方表示

**示例：**
> $\sqrt[9]{3}$ 和 $\sqrt{3}$

**效果：**

```math
 \sqrt[9]{3} <or> \sqrt{3}
```

省略号表示

**示例：**
> $f(x_1, x_2, \ldots, x_n)=x_1^2 + x_2^2+ \cdots + x_n^2$

**效果：**

```math
 f(x_1, x_2, \ldots, x_n)=x_1^2 + x_2^2+ \cdots + x_n^2
```
</font>

### 4. 矢量、积分、极限、累加、累乘、希腊字母
<font size="4">
矢量表示：

**示例：**
> $\vec{a} \cdot \vec{b}=0$

**效果：**

```math
 \vec{a} \cdot \vec{b}=0
```

积分表示

**示例：**
> $\int_0^1x^2{\rm d}x $

**效果：**

```math
 \int_0^1x^2{\rm d}x 
```

极限表示

**示例：**
> $\lim_{n\rightarrow+\infty}\frac{1}{n(n+1)}$

**效果：**

```math
 \lim_{n\rightarrow+\infty}\frac{1}{n(n+1)}
```

累加、累乘表示

**示例：**
> $\sum_1^n\frac{1}{x^2}$， $\prod_{i=0}^n\frac{1}{x^2}$

**效果：**

```math
 \sum_1^n\frac{1}{x^2} , \prod_{i=0}^n\frac{1}{x^2}
```

希腊字母表示

**示例：**
> $$\alpha　A　\beta　B　\gamma　\Gamma　\delta　\Delta　\epsilon　E \varepsilon　　\zeta　Z　\eta　H　\theta　\Theta　\vartheta 

**效果：**

```math
 \alpha,A,\beta,B,\gamma,\Gamma,\delta,\Delta,\epsilon,E,\varepsilon,\zeta,Z,\eta,H,\theta,\Theta,\vartheta
```
</font>

### 5. 常用数学符号
<pre>
<font size="4">
± ：\pm
× ：\times
÷：\div
∣：\mid
⋅：\cdot
∘：\circ
∗: \ast
⨀：\bigodot
⨂：\bigotimes
⨁：\bigoplus
≤：\leq
≥：\geq
≠：\neq
≈：\approx
≡：\equiv
∑：\sum
∏：\prod
∐：\coprod

<b>集合运算符：</b>
∅：\emptyset
∈：\in
∉：\notin
⊂：\subset
⊃ ：\supset
⊆ ：\subseteq
⊇ ：\supseteq
⋂ ：\bigcap
⋃ ：\bigcup
⋁ ：\bigvee
⋀ ：\bigwedge
⨄ ：\biguplus
⨆：\bigsqcup

<b>对数运算符：</b>
log ：\log
lg ：\lg
ln ：\ln

<b>三角运算符：</b>
⊥：\bot
∠：\angle
30∘：30^\circ
sin ：\sin
cos ：\cos
tan ：\tan
cot ：\cot
sec ：\sec
csc ：\csc

<b>微积分运算符：</b>
y′x：\prime
∫：\int
∬ ：\iint
∭ ：\iiint
∬∬：\iiiint
∮ ：\oint
lim ：\lim
∞ ：\infty
∇：\nabla

<b>逻辑运算符：</b>
∵：\because
∴ ：\therefore
∀ ：\forall
∃ ：\exists
≠ ：\not=
≯：\not>
⊄：\not\subset

<b>戴帽符号：</b>
y^ ：\hat{y}
\check{y} ：\check{y}
y˘ ：\breve{y}

<b>连线符号：</b>
a+b+c+d¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯：\overline{a+b+c+d}
a+b+c+d−−−−−−−−−− ：\underline{a+b+c+d} 

<b>箭头符号：</b>
↑：\uparrow
↓：\downarrow
⇑ ：\Uparrow
⇓：\Downarrow
→：\rightarrow
← ：\leftarrow
⇒ ：\Rightarrow
⇐ ：\Leftarrow
⟶ ：\longrightarrow
⟵ ：\longleftarrow
⟹：\Longrightarrow
⟸ ：\Longleftarrow

<b>使用指定字体</b>
{\rm text}如：
使用罗马字体：text ${\rm text}$
其他的字体还有：
\rm　　罗马体　　　　　　　\it　　意大利体
\bf　　黑体　　　　　　　　\cal 　花体
\sl　　倾斜体　　　　　　　\sf　　等线体
\mit 　数学斜体　　　　　　\tt　　打字机字体
\sc　　小体大写字母
</font>
</pre>

 
