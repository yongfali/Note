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

# Redis Basic Using

# Redis 简介

### 1. 第一节
&emsp;&emsp;Redis是一个开源的使用ANSI C语言编写、遵守BSD协议、支持网络、可基于内存亦可持久化的日志型、Key-Value数据库，并提供多种语言的API。

&emsp;&emsp;它通常被称为数据结构服务器，因为值（value）可以是 字符串(String), 哈希(Map), 列表(list), 集合(sets) 和 有序集合(sorted sets)等类型。

**Redis 与其他 key - value 缓存产品有以下三个特点：**

* Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用。 
* Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储。
* Redis支持数据的备份，即master-slave模式的数据备份。

**Redis配置：**

Redis 的配置文件位于 Redis 安装目录下，文件名为 redis.conf。

##### 语法
**Redis CONFIG** 命令格式如下：
> redis 127.0.0.1:6379> CONFIG GET CONFIG_SETTING_NAME

> 使用 * 号获取所有配置项：

##### 编辑配置
你可以通过修改 redis.conf 文件或使用 **CONFIG set** 命令来修改配置。
##### 语法
**CONFIG SET** 命令基本语法：
> redis 127.0.0.1:6379> CONFIG SET CONFIG_SETTING_NAME NEW_CONFIG_VALUE

##### Redis数据类型
Redis支持五种数据类型：string（字符串），hash（哈希），list（列表），set（集合）及zset(sorted set：有序集合)。

### 2. 第二节
##### Redis命令
Redis 命令用于在 redis 服务上执行操作。

要在 redis 服务上执行命令需要一个 redis 客户端。Redis 客户端在我们之前下载的的 redis 的安装包中。

##### 语法
> $ redis-cli

启动 redis 客户端，打开终端并输入命令 **redis-cli**。该命令会连接本地的 redis 服务。

##### 在远程上执行命令

##### 语法
> $ redis-cli -h host -p port -a password

###### 样例
> $redis-cli -h 127.0.0.1 -p 6379 -a "mypass"\
> redis 127.0.0.1:6379\
> redis 127.0.0.1:6379\
> PING

以下实例演示了如何连接到主机为 127.0.0.1，端口为 6379 ，密码为 mypass 的 redis 服务上。

##### Redis 键（Key）
Redis 键命令用于管理 redis 的键。

##### 语法

> redis 127.0.0.1:6379> COMMAND KEY_NAME

##### Redis 字符串(String)
Redis 字符串数据类型的相关命令用于管理 redis 字符串值，基本语法如下：
##### 语法
> redis 127.0.0.1:6379> COMMAND KEY_NAME
##### 实例
> redis 127.0.0.1:6379> SET runoobkey redis\
> OK\
> redis 127.0.0.1:6379> GET runoobkey\
> "redis"

在以上实例中我们使用了 SET 和 GET 命令，键为 runoobkey。

##### Redis 哈希(Hash)
Redis hash 是一个string类型的field和value的映射表，hash特别适合用于存储对象。

##### Redis 列表(List) 
Redis列表是简单的字符串列表，按照插入顺序排序。你可以添加一个元素到列表的头部（左边）或者尾部（右边）
一个列表最多可以包含 232 - 1 个元素 (4294967295, 每个列表超过40亿个元素)。 
##### 实例
> redis 127.0.0.1:6379> LPUSH runoobkey redis\
> (integer) 1\
> redis 127.0.0.1:6379> LPUSH runoobkey mongodb\
> (integer) 2\
> redis 127.0.0.1:6379> LPUSH runoobkey mysql\
> (integer) 3\
> redis 127.0.0.1:6379> LRANGE runoobkey 0 10
> <pre>1) "mysql"
> 2) "mongodb"
> 3) "redis"</pre>

在以上实例中我们使用了 LPUSH 将三个值插入了名为 runoobkey 的列表当中。

##### Redis 集合(Set)
Redis的Set是string类型的无序集合。集合成员是唯一的，这就意味着集合中不能出现重复的数据。\
Redis 中 集合是通过哈希表实现的，所以添加，删除，查找的复杂度都是O(1)。
##### 实例
> redis 127.0.0.1:6379> SADD runoobkey redis\
(integer) 1\
redis 127.0.0.1:6379> SADD runoobkey mongodb\
(integer) 1\
redis 127.0.0.1:6379> SADD runoobkey mysql\
(integer) 1\
redis 127.0.0.1:6379> SADD runoobkey mysql\
(integer) 0\
redis 127.0.0.1:6379> SMEMBERS runoobkey
> <pre>1) "mysql"
> 2) "mongodb"
> 3) "redis"</pre>

在以上实例中我们通过 SADD 命令向名为 runoobkey 的集合插入的三个元素。

##### Redis HyperLogLog
Redis 在 2.8.9 版本添加了 HyperLogLog 结构。

Redis HyperLogLog 是用来做基数统计的算法，HyperLogLog 的优点是，在输入元素的数量

在 Redis 里面，每个 HyperLogLog 键只需要花费 12 KB 内存，就可以计算接近 2^64 个不同元素的基 数。

这和计算基数时，元素越多耗费内存就越多的集合形成鲜明对比。
但是，因为 HyperLogLog 只会根据输入元素来计算基数，而不会储存输入元素本身，所以 HyperLogLog 不能像集合那样，返回输入的各个元素。 

##### 什么是基数?
比如数据集 {1, 3, 5, 7, 5, 7, 8}， 那么这个数据集的基数集为 {1, 3, 5 ,7, 8}, 基数(不重复元素)为5。 基数估计就是在误差可接受的范围内，快速计算基数。 

##### 实例

> redis 127.0.0.1:6379> PFADD runoobkey "redis"
> <pre>1) (integer) 1
> redis 127.0.0.1:6379> PFADD runoobkey "mongodb"
> 2) (integer) 1
> redis 127.0.0.1:6379> PFADD runoobkey "mysql"
> 3) (integer) 1
> redis 127.0.0.1:6379> PFCOUNT runoobkey
> (integer) 3</pre>

##### Redis 事务
Redis 事务可以一次执行多个命令， 并且带有以下两个重要的保证：
 * 事务是一个单独的隔离操作：事务中的所有命令都会序列化、按顺序地执行。
 * 事务在执行的过程中，不会被其他客户端发送来的命令请求所打断。
 * 事务是一个原子操作：事务中的命令要么全部被执行，要么全部都不执行。
 
一个事务从开始到执行会经历以下三个阶段：
* 开始事务。
* 命令入队。
* 执行事务。

##### Redis 事务命令
下表列出了 redis 事务的相关命令：

序号 | 命令及描述
---|---
1.  |DISCARD 事务，放弃执行事务块内的所有命令。
2. |EXEC 行所有事务块内的命令。
3. | MULTI 记一个事务块的开始。
4. | UNWATCH 消 WATCH 命令对所有 key 的监视。
5. | WATCH key [key ...]监视一个(或多个) key ，如果在事务执行之前这个(或这些) key 被其他命令所改动，那么事务将被打断。

##### Redis 脚本
Redis 脚本使用 Lua 解释器来执行脚本。 Reids 2.6 版本通过内嵌支持 Lua 环境。执行脚本的常用命令为 EVAL。 
##### 语法
Eval 命令的基本语法如下： 
> redis 127.0.0.1:6379> EVAL script numkeys key [key ...] arg [arg ...]

##### Redis 连接
Redis 连接命令主要是用于连接 redis 服务。

序号|	命令及描述
-----| ------
1. | AUTH password 证密码是否正确
2. | ECHO message 印字符串
3. | 	PING 看服务是否运行
4. | QUIT 闭当前连接
5. | SELECT index 换到指定的数据库   

### 3. 第三节

##### Redis 数据备份与恢复
Redis SAVE 命令用于创建当前数据库的备份。

##### 语法
> redis 127.0.0.1:6379 > SAVE

该命令将在 redis 安装目录中创建dump.rdb文件。

##### 恢复数据
如果需要恢复数据，只需将备份文件 (dump.rdb) 移动到 redis 安装目录并启动服务即可。获取 redis 目录可以使用 CONFIG 命令，如下所示： 
> redis 127.0.0.1:6379> CONFIG GET dir\
>  1\) "dir"\
>  2\) "/usr/local/redis/bin"

以上命令 CONFIG GET dir 输出的 redis 安装目录为 /usr/local/redis/bin。 
##### Bgsave
创建 redis 备份文件也可以使用命令 BGSAVE，该命令在后台执行。
##### 实例
> 127.0.0.1:6379> BGSAVE

> Background saving started

##### Redis 安全
我们可以通过 redis 的配置文件设置密码参数，这样客户端连接到 redis 服务就需要密码验证，这样可以让你的 redis 服务更安全。 
##### 实例
我们可以通过以下命令查看是否设置了密码验证：
> 127.0.0.1:6379> CONFIG get requirepass

默认情况下 requirepass 参数是空的，这就意味着你无需通过密码验证就可以连接到 redis 服务。

你可以通过以下命令来修改该参数：
> 127.0.0.1:6379> CONFIG set requirepass "runoob"

##### Redis 性能测试
Redis 性能测试是通过同时执行多个命令实现的。
##### 语法
redis 性能测试的基本命令如下：
> redis-benchmark [option] [option value]
##### 实例
> redis-benchmark -h 127.0.0.1 -p 6379 -t set,lpush -n 10000 -q

以上实例中主机为 127.0.0.1，端口号为 6379，执行的命令为 set,lpush，请求数为 10000，通过 -q 参数让结果只显示每秒执行的请求数。

### Redis服务器命令
##### 1. Ping命令：

测试连接是否存活
> redis 127.0.0.1:6379> ping\
> PONG
##### 2. echo命令：

在命令行打印一些内容
> redis 127.0.0.1:6379> echo hello\
> "hello"

##### 3. select命令：
选择数据库。Redis 数据库编号从0~15，我们可以选择任意一个数据库来进行数据的存取。
> redis 127.0.0.1:6379> select 1

表示选择一号数据库

##### 4. quit命令：
退出链接命令。
> redis 127.0.0.1:6379> quit

##### 5. dbsize命令:
查看数据库大小及统计数据库key的数量。
> redis 127.0.0.1:6379> dbsize\
> (integer) 2

##### flushdb命令：
删除当前数据中的所有键值对数据，默认清除的数据是0号数据库的数据。
> redis 127.0.0.1:6379> flushdb\
> OK

##### flushall命令：
删除所有的数据。
> redis 127.0.0.1:6379> flushall\
> OK

### 4. 第四节  持久化
 &emsp;&emsp;Redis的高性能是由于其将所有数据都存储在了内存中，为了使Redis在重启之后仍能保证数据不丢失，需要将数据从内存中同步到硬盘中，这一过程就是持久化。\
 &emsp;&emsp;Redis支持两种方式的持久化，一种是RDB方式，一种是AOF方式。可以单独使用其中一种或将二者结合使用。
##### RDB方式
&emsp;&emsp;RDB方式的持久化是通过快照（snapshotting）完成的，当符合一定条件时Redis会自动将内存中的数据进行快照并持久化到硬盘。
RDB是Redis默认采用的持久化方式，在redis.conf配置文件中默认有此下配置：
> save 900 1\
> save 300 10\
> save 60 10000

&emsp;&emsp;save 开头的一行就是持久化配置，可以配置多个条件（每行配置一个条件），每个条件之间是“或”的关系，“save 900 1”表示15分钟（900秒钟）内至少1个键被更改则进行快照，“save 300 10”表示5分钟（300秒）内至少10个键被更改则进行快照。

在redis.conf中：
> 配置dir指定rdb快照文件的位置\
> 配置dbfilenam指定rdb快照文件的名称

&emsp;&emsp;Redis启动后会读取RDB快照文件，将数据从硬盘载入到内存。根据数据量大小与结构和服务器性能不同，这个时间也不同。通常将记录一千万个字符串类型键、大小为1GB的快照文件载入到内存中需要花费20～30秒钟。
##### AOF方式
&emsp;&emsp;默认情况下Redis没有开启AOF（append only file）方式的持久化，可以通过appendonly参数开启：

appendonly yes

&emsp;&emsp;开启AOF持久化后每执行一条会更改Redis中的数据的命令，Redis就会将该命令写入硬盘中的AOF文件。AOF文件的保存位置和RDB文件的位置相同，都是通过dir参数设置的，默认的文件名是appendonly.aof，可以通过appendfilename参数修改：appendfilename appendonly.aof

### 5. 第五节 主从复制
&emsp;&emsp;持久化保证了即使redis服务重启也会丢失数据，因为redis服务重启后会将硬盘上持久化的数据恢复到内存中，但是当redis服务器的硬盘损坏了可能会导致数据丢失，如果通过redis的主从复制机制就可以避免这种单点故障。

#### 主从配置
##### 主redis配置
无需特殊配置。
##### 从redis配置
修改从redis服务器上的**redis.conf**文件，添加slaveof 主**redisip** 主**redis端口**
> \# slaveof <masterIp> <masterPort> 

> slveof 192.168.1.20 6397

上边的配置说明当前该从redis服务器所对应的主redis是192.168.1.20，端口是6379

##### 全复制过程
1. slave 服务启动，slave 会建立和master 的连接，发送sync 命令。
2. master启动一个后台进程将数据库快照保存到RDB文件中。（**注意：此时如果生成RDB文件过程中存在写数据操作会导致RDB文件和当前主redis数据不一致，所以此时master 主进程会开始收集写命令并缓存起来。**）
3. master 就发送RDB文件给slave。
4. slave 将文件保存到磁盘上，然后加载到内存恢复。
5. master把缓存的命令转发给slave。(**注意：后续master 收到的写命令都会通过开始建立的连接发送给slave。当master 和slave 的连接断开时slave 可以自动重新建立连接。如果master 同时收到多个slave 发来的同步连接命令，只会启动一个进程来写数据库镜像，然后发送给所有slave。**)

##### 部分复制：
&emsp;&emsp;从机连接主机后，会主动发起 PSYNC 命令，从机会提供 master的runid(机器标识，随机生成的一个串) 和offset（数据偏移量，如果offset主从不一致则说明数据不同步），主机验证 runid 和 offset 是否有效， runid相当于主机身份验证码，用来验证从机上一次连接的主机，如果runid验证未通过则，则进行全同步，如果验证通过则说明曾经同步过，根据offset同步部分数据。

# Monogodb Basic Using

### 第一章 简介
##### 什么是MongoDB?
MongoDB 是由C++语言编写的，是一个基于分布式文件存储的开源数据库系统。在高负载的情况下，添加更多的节点，可以保证服务器性能。

MongoDB 旨在为WEB应用提供可扩展的高性能数据存储解决方案。

MongoDB 将数据存储为一个文档，数据结构由键值(key=>value)对组成。MongoDB 文档类似于 JSON 对象。字段值可以包含其他文档，数组及文档数组。
##### MongoDB下载
你可以在mongodb官网下载该安装包，地址为：https://www.mongodb.com/download-center#community。
MonggoDB支持以下平台:

##### MongoDB连接
> mongodb://[username:password@]host1[:port1][,host2[:port2],...[,hostN[:portN]]][/[database][?options]]

* mongodb:// 这是固定的格式，必须要指定。
* username:password@ 可选项，如果设置，在连接数据库服务器之后，驱动都会尝试登陆这个数据库
* host1 必须的指定至少一个host, host1 是这个URI唯一要填写的。它指定了要连接服务器的地址。如果要连接复制集，请指定多个主机地址。
* portX 可选的指定端口，如果不填，默认为27017
* /database 如果指定username:password@，连接并验证登陆指定数据库。若不指定，默认打开 test 数据库。
* ?options 是连接选项。如果不使用/database，则前面需要加上/。所有连接选项都是键值对name=value，键值对之间通过&或;（分号）隔开 

##### 更多连接实例
1. 连接本地数据库服务器，端口是默认的。
   > mongodb://localhost
2. 使用用户名fred，密码foobar登录localhost的admin数据库
   > mongodb://fred:foobar@localhost
3. 使用用户名fred，密码foobar登录localhost的baz数据库。
   > mongodb://fred:foobar@localhost/baz
4. 连接 replica set 三台服务器 (端口 27017, 27018, 和27019):
   > mongodb://localhost,localhost:27018,localhost:27019 q
5. 连接 replica set 三台服务器,写入操作应用在主服务器并且分布查询到从服务器。
   > mongodb://host1,host2,host3/?slaveOk=true
6. 直接连接第一个服务器，无论是replica set一部分或者主服务器或者从服务器。
   > mongodb://host1,host2,host3/?connect=direct;slaveOk=true
7. 以安全模式连接到replica set，并且等待至少两个复制服务器成功写入，超时时间设置为2秒。
   > mongodb://host1,host2,host3/?safe=true;w=2;wtimeoutMS=2000

### 第二章 MongoDB的CRUD操作
#### 2.1 创建数据库
> use DATABASE_NAME

如果数据库不存在，则创建数据库，否则切换到指定数据库。如果你想查看所有数据库，可以使用 **show dbs** 命令。
#### 2.2 数据库删除
> db.dropDatabase()

删除当前数据库，默认为 test，你可以使用 db 命令查看当前数据库名。

##### 创建集合
> db.createCollection(Name)

##### 删除集合
> db.collection.drop()

其中collection为集合的名字

#### 2.3 插入文档
MongoDB 使用 insert() 或 save() 方法向集合中插入文档，语法如下：
> db.COLLECTION_NAME.insert|save(document)

如果该集合(COLLECTION_NAME)不在该数据库中， MongoDB 会自动创建该集合并插入文档。插入完成后，可以通过如下命令查看插入的文档。
> db.COLLECTION_NAME find()

还能执行单条和多条数据的插入
> db.collection.insertOne():向指定集合中插入一条文档数据\
> db.collection.insertMany():向指定集合中插入多条文档数据

#### 2.4 更新文档
**uddate() 方法**
<pre>db.collection.update(
   <query>,
   <update>,
   {
     upsert: <boolean>,
     multi: <boolean>,
     writeConcern: <document>
   }
)
</pre>

参数说明：
* **query** : update的查询条件，类似sql update查询内where后面的。
* **update** : update的对象和一些更新的操作符（如$,$inc[增加],$set[设置]...）等，也可以理解为sql update查询内set后面的。
* **upsert** : 可选，这个参数的意思是，如果不存在update的记录，是否插入objNew,true为插入，默认是false，不插入。
* **multi** : 可选，mongodb 默认是false,只更新找到的第一条记录，如果这个参数为true,就把按条件查出来多条记录全部更新。
* **writeConcern** :可选，抛出异常的级别。

**save() 方法**

save() 方法通过传入的文档来替换已有文档。语法格式如下：
<pre>
db.collection.save(
   <document>,
   {
     writeConcern: <document>
   }
)
</pre>
参数说明：
* **document** : 文档数据。
* **writeConcern** :可选，抛出异常的级别。

#### 2.5 删除文档
MongoDB remove()函数是用来移除集合中的数据，其语法格式如下。
<pre>
    db.collection.remove(
   <query>,
   {
     justOne: <boolean>,
     writeConcern: <document>
   }
)
</pre>
参数说明：
* **query** :（可选）删除的文档的条件。
* **justOne** : （可选）如果设为 true 或 1，则只删除一个文档。
* **writeConcern** :（可选）抛出异常的级别。

#### 2.6 查询文档
MongoDB 查询文档使用find()方法
> db.collection_name.find(query,projection)

参数说明：
* query 查询条件，可选。
* 可选，使用投影操作符指定返回的键。查询时返回文档中所有键值， 只需省略该参数即可（默认省略）。

对于数据可以格式化输出显示。
> db.collection_name.find().pretty()

MongoDB 与 RDBMS Where 条件查询比较
操作 | 格式 | 实例 | 对应SQL语句
---|---|---|---
等于 | {<key> : <value> } | db.col.find({"by":"菜鸟教程"}).pretty() |where by = '菜鸟教程'
大于 | {<key> : {$gt : <value>}} |  db.col.find({"likes":{$gt:50}}).pretty() | where likes > 50
小于 |  {<key> : {$lt : <value>} | db.col.find({"likes":{$lt:50}}).pretty() | where likes < 50
大于等于 | {<key>:{$gte:<value>}} | db.col.find({"likes":{$gte:50}}).pretty() | where likes >= 50
小于等于 | {<key>:{$lte:<value>}} | db.col.find({"likes":{$lte:50}}).pretty() | where likes <= 50
不等于 | {<key>:{$ne:<value>}} | db.col.find({"likes":{$ne:50}}).pretty() |where likes != 50

##### MongoDB AND 查询
MongoDB 的 find() 方法可以传入多个键(key)，每个键(key)以逗号隔开，及常规 SQL 的 AND 条件。
> db.col.find({key1:value1, key2:value2}).pretty()

##### MongoDB OR 查询
MongoDB OR 条件语句使用了关键字 $or,语法格式如下：
<pre>
>db.col.find(
   {
      $or: [
         {key1: value1}, {key2:value2}
      ]
   }
).pretty()
</pre>
> 

##### MongoDB Limit()查询：
> \> db.COLLECTION_NAME.find().limit(NUMBER)

**NUMBER**：为指定查询显示的记录数量

##### MongoDB Skip()查询：
> \> db.COLLECTION_NAME.find().skip(NUMBER)

**NUMBER**：为指定跳过查询的记录条数，从跳过指定数目的记录后开始查询。

##### MongoDB sort()排序查询：
在MongoDB中使用使用sort()方法对数据进行排序，sort()方法可以通过参数指定排序的字段，并使用 1 和 -1 来指定排序的方式，其中 1 为升序排列，而-1是用于降序排列。
> \> db.COLLECTION_NAME.find().sort({KEY:1})

#### 2.7 MongODB 数据备份和还原

##### 数据备份
在Mongodb中我们使用**mongodump**命令来备份MongoDB数据。该命令可以导出所有数据到指定目录中。\
**mongodump**命令可以通过参数指定导出的数据量级转存的服务器。
> mongodump -h dbhost -d dbname -o dbdirectory

* **-h** 主机名
* **-d**  要备份的数据库名字
* **-o** 备份后数据存贮的位置

##### 数据还原
mongodb使用 **mongorestore** 命令来恢复备份的数据。
> mongorestore -h <hostname><:port> -d dbname <path>

#### 2.8 MongoDB监控
&emsp;&emsp;在你已经安装部署并允许MongoDB服务后，你必须要了解MongoDB的运行情况，并查看MongoDB的性能。这样在大流量得情况下可以很好的应对并保证MongoDB正常运作。MongoDB中提供了**mongostat** 和**mongotop** 两个命令来监控MongoDB的运行情况。
> D:\set up\mongodb\bin>mongostat

> D:\set up\mongodb\bin>mongotop

### 第三章 MongoDB 高级教程
#### 3.1 MongoDB 原子操作
&emsp;&emsp;mongodb不支持事务，所以，在你的项目中应用时，要注意这点。无论什么设计，都不要要求mongodb保证数据的完整性。

&emsp;&emsp;但是mongodb提供了许多原子操作，比如文档的保存，修改，删除等，都是原子操作。

&emsp;&emsp;所谓原子操作就是要么这个文档保存到Mongodb，要么没有保存到Mongodb，不会出现查询到的文档没有保存完整的情况。

#### 3.2 MongoDB 正则查找
> db.collection_name.find(field:{$regx:"对应正则表达式"})

#### 3.3 Monogodb 管理工具Rockmongo
RockMongo是PHP5写的一个MongoDB管理工具。通过 Rockmongo 你可以管理 MongoDB服务，数据库，集合，文档，索引等等。它提供了非常人性化的操作。类似 phpMyAdmin（PHP开发的MySql管理工具）。

下载地址：[Rockmongo下载](http://rockmongo.com/downloads)


 
