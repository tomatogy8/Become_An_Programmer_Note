# Day01-HTML01

<!-- toc -->

## 01-计算机基础知识

### 01-1 文件和文件夹管理

* 掌握文件和文件夹的管理，包括创建、删除、重命名、复制、粘贴、剪切、移动。

* 掌握"文件扩展名"的意义

* 在Windows下,所有的文件的名字，是两部分组成的。语法

```
文件名.扩展名
```

> 扩展名一般就是2~4个字母,表示文件的格式。比如`.jpg`是图片格式，`.mp3`是音乐格式，`.doc`文档
> **一般来说，操作系统是不主动显示扩展名的，需要我们自己设置**

* Windows 7:

![01](images/section01/01.png)

![02](images/section01/02.png)

* Windows 10:

![09](images/section01/09.png)

* OS X 10.9:

![10](images/section01/10.png)

![11](images/section01/11.png)

* 知道"打开方式"的意义

一个文件，可以用多种软打开，这就叫做打开方式

![03](images/section01/03.png)

![04](images/section01/04.png)

实际上现在你就应该树立一种思维，同一个文件可以用不同软件打开。

比如:**`.jpg`用照片查看器打开，就是浏览模式；用画图打开，就是编辑模式**

* 会使用桌面，知道"快捷方式"的概念

注意，桌面是一个特殊的文件夹。这个文件夹路径：`C:\Users\yh\Desktop`

![05](images/section01/05.png)

快捷方式是什么？程序快速打开的一个入口，双击就能打开程序

![06](images/section01/06.png)

所有快捷方式，都有一个小箭头图标。就是一个快捷入口，所以删除这个图标，程序还在

### 01-2 特殊按键和快捷键

键盘上除了有字母、数字之外，还有一些特殊的按键：Ctrl、Shift、Alt、Tab

* Ctrl键是英语control"控制"的意思，这个按键，单独按没有任何作用，都要和其他的按键一起按才有用。比如ctrl+c，表示同时按住ctrl键和c键，一会儿将知道这个功能是复制。
* Shift键是英语shift"换挡"的意思，按下这个按键同时击打字母，打出的就是大写字母。**熟悉shift键来打大写字母，尽量少用大小写锁定键。**
* Alt键是英语altemate"调整"的意思，和ctrl一样，自己按没啥用，都要和其他的按键一起按才有用。比如alt+f4，表示关闭当前的窗口，比如你正在玩儿游戏，老板来了，可以啊alt+f4快速关闭窗口。
* Tab键是用于tab"制表符"的意思，经常实现"切换的功能"。比如我们再word软件中同时打开了两个文档，可以用ctrl+tab键，来在两个文档之间切换。当然，可以用alt+tab键来切换程序。

必须掌握的快捷键：

* Ctrl+C 		复制
* Ctrl+V 		粘贴
* Ctrl+X	        剪切（就是移动文件，在原来的文件夹ctrl+x一个文件，然后在新文件夹中ctrl+v粘贴）
* Ctrl+Tab        切换（具体切换什么，要看是什么软件）
* Alt+F4            关闭程序
* F2                   重命名 
* F5                   刷新，比如看网页的时候，想刷新网页，按F5
* Ctrl+Z            撤销，就是这一步干错了，就ctrl+z撤销
* Windows+E 打开资源管理器 
* Windows+D 显示桌面
* Ctrl + 空格  切换中英文，严禁用shift键切换 

![07](images/section01/07.png)

### 01-3 打字速度

打字速度是必备的素养！

* 严禁二指神功，必须养成正确的指法；比如打{时，要按住shift+[。正确的按键方法，是左手小拇指按住左边的shift键，右手中指按[键。
* 金山打字通，只需要练习英文打字，要求英文文章一定要练习到每分钟100字以上

## 02-互联网的原理

### 02-1 上网就是请求数据

网页上的内容，怎么就被我们看见了？什么是上网？

> 我们先不直接解决这个问题，我们做一个小实验。我们每个人的电脑里面，都有一个神秘的文件夹：`C:\Users\yh\AppData\Local\Microsoft\Windows\Temporary Internet Files`这个文件夹叫做临时文件夹（**文件夹知道存在就还好了，不用你自己查找**）

我们清空这个文件夹中的全部内容

![08](images/section01/08.png)

我们打开IE浏览器，看几个网页。结果，这个文件夹中又多了很多的内容：


通过这个实验，目前为止，我们可以得出结论，上网的时候，是有真实的、物理的文件传输的！

所以我们经常感觉第二次打开网页，比第一次快，这是因为第一次打开网页的时候，所以得图片都已经存过来了。

所以我们也能够解释，为什么每次都用CCleaner能清理一堆垃圾，释放很多硬盘空间。

**我们发现，浏览了一个Google首页，就出现那么多的文件，所以现在我们的幼小的心灵中，就要有一个初步认识，网页不是一个文件，而是一堆文件。**

我们可以回答刚才的问题了，"上网"究竟是什么？答案：上网就是请求数据，就是文件传输

> 服务器上存放着网页的相关文件，包括html文件、css文件、js文件、图片等。当我们打开浏览器，输入网址，我们的计算机就会对这些文件发出HTTP请求。
> 服务器收到请求之后，会把这些文件通过HTTP协议，传输到我们的计算机中（保存到了刚才那个临时文件夹中）。这些文件，将在我们的计算机本地的浏览器中，进行渲染、呈递。

也就是说，本来人家文件好好的在服务器上睡大觉，你一输入网址，就把这些文件传输到本地计算机来了。这些文件在本地的计算机中，进行渲染，展示。

### 02-2 服务器

* 服务器就是计算机，只不过比我们用的笔记本的配置牛逼了很多，并且24小时不断电，不关机。
* 服务器上存储着网页的相关文件。一旦有访问者浏览网站，服务器就将发生这些文件给访问者。
* 服务器一旦关机，网站就无法访问了。
* 服务器的更多知识，我在讲到Ajax的知识后再补充。现在只需要了解基本概念就OK

![](images/section01/36.png)

### 02-3 浏览器

![](images/section01/37.png)

* 浏览器是按照再客户的电脑里面的，是一个软件，能够让用户上网。
* 浏览器有版本之分，有浏览器兼容问题。后面实际项目会讨论这个问题

### 02-4 HTTP

* 超文本传输协议，Hypertext Transfer Protocol.

>  这是一个文件的传输协议，我们上网的时候，所有的文件都是通过HTTP这个协议，从服务器上传输到客户的电脑里面的。

现在，我们只需要知道这些即可，Ajax上会详细讲解HTTP这个东西

> 后面我会给你讲如何购买www域名和空间，全年100元以内。

现在我们必须要树立一个思想，就是每一个网址，都对应着确定的服务器上的文件。

比如网址:

```
http://www.yhyangjiabin.tech/1.html
```

就是服务器上面的1.html文件

```
http://www.yhyangjiabin.tech/
```

看似没有精确到一个文件，但是有一个规定，就是index.html是默认的首页文件

index就是英语"目录"的意思。

```
http://www.yhyangjiabin.tech/aaa/b.html
```

服务器上面有一个aaa文件夹，这个文件夹里面有一个b.html文件。

上面的都没听懂没事，记住下面内容就好

**网页是真实物理的文件。并且一个是很多的物理文件组成的：html文件、图片文件、js文件、css文件。这些文件要通过特殊软件才能上传到服务器上。然后就能让用户看了。用户通过浏览器，访问网址，服务器上面的文件就会通过http请求悄悄地传输用户的电脑中的临时文件夹中，在用户的电脑中执行、渲染、呈递。**

## 03-开发环境配置

### 03-1 Windows 7 配置

* Windows电脑适用：针对硬件比较低的电脑,我们关闭一些Windows的功能和动画效果

打开控制面板，选择系统与安全。接下来如下图所示：

![](images/section01/12.png)

* Windows7需要安装.NET Framework 4.x版本以上，Windows 10需要安装.NET Framwork 3.5

### 03-2 Lantern和Proxifier 配置

> 配置这两个工具，是方便我们查阅资料（Google、GitHub、StackOverflow、Wikipedia），push代码到GitHub远程仓库

* Lantern安装和配置

Lantern下载地址：https://getlantern.org/en_US/

勾选代理所有流量，并记下代理地址和端口号

![](images/section01/13.png)

![](images/section01/14.png)

* Proxifier安装和配置

Proxifier下载地址：https://www.proxifier.com/

key:KFZUS-F3JGV-T95Y7-BXGAS-5NHHP

增加代理地址：

![](images/section01/15.png)

新建代理规则：

![](images/section01/16.png)

修改DNS hostname：

![](images/section01/17.png)

### 03-3 Git和GitHub 配置

> 安装Git是作为我们版本控制工具（简单理解为存储我们修改过的内容，存储多个版本后。需要用一个管理工具，所以我们选择Git），我们在本地操作GitBook，需要用到Git Bash这个组件。GitHub这个是远程仓库的一个著名网站。

* Git的安装配置

Git的下载地址：https://git-scm.com/

和一般应用安装类似，修改路径，一直下一步就OK。

Git Bash配置：

修改字体和字号大小：

修改编码格式：

![](images/section01/18.png)

![](images/section01/19.png)

修改主题样式，修改路径`/c/Users/yh`下 的`.minttyrc`文件

```
BoldAsFont=-1
Locale=C
Charset=UTF-8
FontHeight=14
BackgroundColour=13,25,38
ForegroundColour=217,230,242
CursorColour=217,230,242
Black=0,0,0
BoldBlack=38,38,38
Red=184,122,122
BoldRed=219,189,189
Green=122,184,122
BoldGreen=189,219,189
Yellow=184,184,122
BoldYellow=219,219,189
Blue=122,122,184
BoldBlue=189,189,219
Magenta=184,122,184
BoldMagenta=219,189,219
Cyan=122,184,184
BoldCyan=189,219,219
White=217,217,217
BoldWhite=255,255,255
FontHeight=14
```

* GitHub网站，GitHub Desktop安装和配置

GitHub网站：注册一个账号，**注册完成后，记得点击激活邮件的按钮或链接**，设置第二个邮箱（作为**展示邮箱**和配置链接本地电脑的邮箱，可以选择国内邮箱。**注册邮箱不要选择国内邮箱**）

GitHub Desktop安装和配置：

GitHub Desktop下载地址：https://desktop.github.com/

登陆GitHub账号：

![](images/section01/20.png)

配置GIt的用户名和邮箱（这里的邮箱填我们在GitHub上的**展示邮箱**）

![](images/section01/21.png)

![](images/section01/22.png)

![](images/section01/23.png)

**测试本地电脑和GitHub网站正常通信，我们需要**Lantern和Proxifier**配合**

新建一个本地仓库，增加README文件。并push到GitHub的远程仓库

### 03-4 GitBook和Markdown 配置

* GitBook（现阶段，主要记录我们学习笔记）的安装和配置

下载Node.js（先不解释，这是我们后面要学习的一个东西。我们现在这里用一下）：https://nodejs.org/en/

**选择LTS版本,长期支持版本**

验证是否按照成功

```bash
node -v

# 输出
v8.9.3

npm -v

# 输出
5.5.1
```

![](images/section01/24.png)

GitBook CLI安装

```bash
npm install -g gitbook-cli
```

GitBook安装和初始化GitBook书籍仓库

```bash
gitbook init Become_An_Programmmer_Note
```

![](images/section01/25.png)

增加`book.json`,配置笔记主要信息

```json
touch book.json // 创建书籍配置文件


// book.json
{
    "title": "如何成为一个开发者指导",
    "description": "学习如何为一个开发者,用最简单的前端知识作为基础",
    "language": "zh" ,
    "pdf": {
        "toc": true,
        "pageNumbers": false,
        "fontSize": 14,
        "paperSize": "a4",
        "margin": {
            "right": 62,
            "left": 62,
            "top": 36,
            "bottom": 36
        }
    },
    "plugins": [
        "prism",
        "-highlight"
    ] 
}
```

完成上面书籍配置文件，安装代码高亮插件。在书籍根目录执行下面命令：

```bash
gitbook install
```

![](images/section01/26.png)

增加书面封皮：

根目录下存两张图片（尺寸）：cover.jpg（1800x2360）、cover_small.jpg（200x262）

初始化一个Git仓库，增加忽略文件，并push到GitHub上

```bash
git init // 在书籍的根目录下执行

touch .gitignore

// .gitignore
# Node rules:
## Grunt intermediate storage (http://gruntjs.com/creating-plugins#storing-task-files)
.grunt

## Dependency directory
## Commenting this out is preferred by some people, see
## https://docs.npmjs.com/misc/faq#should-i-check-my-node_modules-folder-into-git
node_modules

# Book build output
_book

# eBook build output
output


# push GitHub
```

* 预览书籍

```bash
gitbook serve // 预览书籍

# 输出内容
Starting server ...
Serving book on http://localhost:4000
```

允许防火墙通过

![](images/section01/27.png)

成功预览

![](images/section01/28.png)

push到GitHub的远程仓库中

![](images/section01/29.png)

![](images/section01/30.png)

![](images/section01/31.png)

* 输出电子书籍格式ePub, Mobi, PDF

**Windows下的方法：安装Calibre应用，然后输入在书籍跟目录下输入下面命令**

**Windows下必须在Git Bash中输入,才能正确输出,如果报错。安装完Calibre，运行一次，再执行下面命令**

Calibre 下载地址：https://calibre-ebook.com/download

```bash
# Generate a PDF file
$ gitbook pdf ./ ./output/Become_An_Programmer_Note.pdf

# Generate an ePub file
$ gitbook epub ./ ./output/Become_An_Programmer_Note.epub

# Generate a Mobi file
$ gitbook mobi ./ ./output/Become_An_Programmer_Note.mobi
```

* 常用Markdown语言，后面有需要在增加语法

标题

```markdown
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag
```

项目符号

```markdown
* Item 1
* Item 2
  * Item 2a
  * Item 2b
```

代码和代码块

```markdown
```
function test() {
  console.log("notice the blank line before this function?");
}
```
```

加粗

```markdown
**This text will be bold**
```

引用

```markdown
> the present is our past.
```

图片

```markdown
![gras](img/image.jpg)
```

表格

```markdown
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

### 03-5 Visual Studio Code和Chrome、Firefox配置

* Visual Studio Code（作为代码编辑器和笔记记录工具）安装和配置

任何的纯文本编辑器都能够编辑html，比如记事本、editplus、notepad++。 

比较有名的专门制作网页的工具有： 

Visual Studio Code （我决定把主要开发工具转到Visual Studio 下所有，就用了Code。没有其他原因）

Sublime （高效率的程序书写工具，我以前最喜欢的用的代码编辑器） 

WebStorm （更高级的项目级别编程工具）

> 不管用什么编辑器，你都要知道，做网页和工具无关，任何的纯文本编辑器都能够做网页。我们学习的是代码，而不是所谓的工具。不过，不可否认，一个好的工具，确实能够提高工作效率，代码书写的速度，但是本质上讲，记事本也能书写网页。 

Visual Studio Code 下载地址：https://code.visualstudio.com/

![](images/section01/31.png)

* Visual Studio Code Tips:
    * 多行编辑快捷键:Shift + Alt + 鼠标左键选取要编辑的内容
    * Tab键自动生成标签对儿
    * 设置工作区,分别放置两个文件夹存储Note和Code
    * 设置文字显示大小为14
    * 安装插件
        * Cobalt2 Theme Official 主题
        * Path Intellisense 路径提示
        * vscode-icons 图标

* Chrome安装和配置

Chrome下载地址：https://enterprise.google.com/chrome/chrome-browser/

* Firefox安装和配置

Firfox下载地址：https://www.mozilla.org/en-US/firefox/all/

## 04-HTML初步认识

### 04-1 认识什么是纯文本文件txt

Windows中自带一个软件，叫做记事本。记事本保存的文档格式就是txt格式，就是英语text的缩写。术语上，称呼这个文件叫做"纯文本文件"。

我们做个实验，**发现doc这个文件能够保存内容和样式，字有红的、蓝的。但是txt格式有点不同**

我看到的：

![](images/section01/38.png)

>我只是改变了软件的设置，而没有改变txt这个文件的设置。txt文件压根就不能设置样式

你看到的：

![](images/section01/39.png)

**txt文件，只能保存文本内容，是无法记录文本样式的。**

所以，docx和txt存储同样的内容，docx比txt大：

存储相同内容：路遥知马力，日久见人心

![](images/section01/40.png)

> 纯文本文件就是这样的文件
> * 只有文本，没有样式
> * 用记事本等纯文本编辑器可读，不是乱码

结论：html、css、js都是纯文本的。

### 04-2 HTML是负责描述文档语义的语言

**HTML是英语HyperText Markup Language的缩写，超文本标记语言。**

**HTML就是网页的格式**

现在，来制作我们人生中第一个网页

新建一个txt文件：

也就是说，html本质上和txt没有任何区别，他们都是纯文本文件。

我们强行把这个文件的扩展名，从txt更改为html，我们会发现小图标就变成浏览器的小图标了：

![](images/section01/41.png)

在"打开方式"中，用记事本可以编辑它。

现在要养成**编辑器里面编辑->保存Ctrl + S->浏览器里面刷新F5**的习惯

![](images/section01/42.png)

html到底干嘛用的，看一下例子：

![](images/section01/33.png)

纯文本txt文件是不能描述稳定的语义的，文档中不知道谁是主标题，谁是副级标题，是谁段落。所以html应运而生。

下面就是一个html文件的演示，就是通过html标签对儿，来给文本增加语义

```html
<html>
	<head>
		<meta charset="UTF-8">
		<title>天问</title>
	</head>
	<body>
	<h1>天问（一）<h1>
		<p>曰遂古之初，谁传道之？</p>
		<p>上下未形，何由考之？</p>
		<p>冥昭瞢暗，谁能极之？</p>
		<p>冯翼惟像，何以识之？</p>
		<p>明明暗暗，惟时何为？</p>
		<p>阴阳三合，何本何化？</p>
		<p>圜则九重，孰营度之？</p>
		<p>惟兹何功，孰初作之？</p>
		<p>斡维焉系，天极焉加？</p>
		<p>八柱何当，东南何亏？</p>
		<p>九天之际，安放安属？</p>
		<p>隅隈多有，谁知其数？</p>
		<p>天何所沓？十二焉分？</p>
		<p>日月安属？列星安陈？</p>
		<p>出自汤谷，次于蒙泛。</p>
		<p>自明及晦，所行几里？</p>
		<p>夜光何德，死则又育？</p>
		<p>厥利维何，而顾菟在腹？</p>
		<p>女歧无合，夫焉取九子？</p>
		<p>伯强何处？惠气安在？</p>
	</body>
</html>
```

html提供了很多标签对儿，可以给文本增加不同的语义。比如：

`<h1></h1>`标签对儿，主标题

`<h2></h2>`标签对儿，二级标题

`<p></p>`标签对儿，段落


现在的业界的标准，网页技术严格的三层分离：**html就是负责描述页面的语义；css负责描述页面的样式；js负责描述页面的动态效果的。**

所以，html不能让文字居中，不能更改文字字号、字体、颜色。因为这些都是属于样式范畴，都是css干的事情；html不能让盒子运动起来，因为这些属性行为范畴，都是js干的事儿。

html只能干一件事情，就是通过标签对儿，给文本增加语义。这是html唯一能做的。

**html中，除了语义，其他什么都没有。**

html是一个纯文本文件（就是用txt文件改名而成），用一些标签来描述文字的语义，这些标签在浏览器里面是看不到的，所以称为"超文本"，所以就是"超文本标记语言"了。

所以，接下来，我们就要学习一堆html的标签对儿，这些标签对儿能够给文本不同的语义。

标签对儿是由起始标签和结束标签组成的：

```html
<h1>天问（一）<h1>
```

`<h1>` 起始标签

`</h1>` 结束标签

> 比如：现在问你，h1标签有什么作用？
> 正确答案：给文本增加主标题的语义
> 错误答案：给文字加粗、加黑、变大


## 05-HTML骨架和基本语法

html有基本骨架，这个骨架能够用VS Code快速生成

![](images/section01/35.png)

骨架抽象出来：

```html
<html>
    <head>
    </head>
    <body>
    </body>
</html>
```

网页的最外层的标签对儿是`<html></html>`标签对儿，里面有两部分，分别是head和body。

`head`标签中，描述网页的配置；`body`中的内容，才是用户可以看见的内容。

完整的骨架：

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8" />
    <title>我是标题</title>
</head>
<body>
    <h1>我是一个主标题</h1>
    <p>我是一个段落</p>
</body>
</html>
```

* 第1行，就是网页的声明头，这行语句，千万不要背诵，谁背谁傻。术语叫做DocType Defintion，文档类型定义，简称DTD。这行语句非常的复杂，里面暗含了一个网址。W3C就是出web规范的组织机构。html、css、js的规范都是W3C定义发布的。world wide web coalition , 国际万维网联盟。网页声明头可以告诉浏览器，这是一个什么标准的页面。 

* 第2行，是最大的`html`标签，所有的网页内容，都要包裹在这个标签对儿里面。 

* 我们发现，html标签中，有两个属性： 
    * `xmlns="http://www.w3.org/1999/xhtml" `  命名空间，就是一个规范； 
    * `xml:lang="en"`  语言是英语 

* 第3行，就是head标签，就是配置。 

* 第4行，`<meta http-equiv="Content-Type" content="text/html;charset=UTF-8"> `字符集的配置 

* 第5行，`<title>我是标题</title>`  网页的标题，可以显示在浏览器的标签栏中。 

* 第7行，`body`标签就是网页的内容，用户能够看见。 