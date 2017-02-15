# **上海创蓝WEB前端开发规范手册**

[TOP]

## **前言**
### 规范目的

为提高团队协作效率，便于后端人员添加功能及前端后期优化维护，输出高质量的文档，特制订此文档。本规范文档一经确认，前端开发人员必须按照本文档规范进行前端页面开发。本文档如有不对或者不合适的地方请及时提出。
>- 规范不是一种约束，而是一种约定，强调团队的一致性
>- 加强团队的合作性，提高协作效率
>- 形成一种团队文化，积累知识
>- 规范最终是为项目服务的，我们所做的一切都是为了优化项目和流程提高我们的工作效率


### 基本准则
符合W3C（万维网联盟http://www.w3c.org）定义的Web标准，包括结构标准HTML、表现语言标准CSS、行为标准DOM和ECMAScript，必须通过W3C的HTML和CSS标准验证。 
总体要求为：符合web标准，语义化html，结构、表现、行为分离，兼容性优良，页面性能良好，代码简洁有序，尽可能的减少服务器负载，保证最快的解析速度。


### 黄金定律
 不管有多少人共同参与同一个项目，一定要确保每一行代码都像是同一个人编写的。尽量遵循标准和语义，但是不要以牺牲实用性为代价。任何时候都要尽量使用最少的标签和元素并保持最小的复杂度。

### 谨记
切勿原封不动复制他人代码，不根据页面需求添加样式，标签，js。避免一切导致页面冗余的代码。复制他人代码前，必须理解每行代码的含义，并根据页面所需做相应调整。


## **一般规范**
### 文件规范
**1.文件存放**(没有特殊要求时，建议文件存放方法,根目录暂指静态目录)

>- html文件放在根目录下面。
>- 在根目录下新建css文件夹，所有的css文件放在此目录下。
>- 在根目录下新建js文件夹，所有的js文件放在此目录下，在该目录下新建plugins文件夹，存放使用到的插件js文件。
>- 在根目录下新建images文件，所有的图片文件放在此目录下。
>- 在根目录下新建fonts文件夹，所有的字体文件放在此目录下。
>- 其他文件酌情处理。
>- css、js和图片文件较多时，在其相应的目录下建立子目录，分别存放。
>- 使用到的插件css和插件js文件一个目录。


**2.文件名称**
>- 统一用小写的英文字母、数字和下划线的组合。
>- 确保文件命名总是以字母开头而不是数字。
>- 其中不得包含汉字、空格和特殊字符。
>- 使用英文命名，需能够通过文件名称方便的理解每一个文件的意义。
>- 需要对文件增加前后缀或特定的扩展名（比如 .min.js, .min.css）。这种情况下，使用点分隔符来区分这些在文件名中带有清晰意义的元数据。
>
>**不推荐**
>``` python
>Myscript.js
>myCamelCaseName.css
>1001_scripts.js
>my_file_min.css
>```
>**推荐**
>``` python
>my_script.js
>my_camel_case_name.css
>scripts_1001.js
>my_file.min.css
>```

**3.图片文件命名**
>- 图片的名称分为头尾两部分，用下划线隔开，头部分表示此图片的大类性质。eg : `banner`, `logo` , `button` , `menu`
>- 尾部表示此图片的小类性质或者属性等。eg：`banner_sohu.jpg` , `menu_off`。

**4.css和js文件**
占用空间较大时，在上线前使用压缩工具压缩，在线使用压缩版本。

**5.图片格式**仅限于 `jpg` , `png` , `gif`。图片文件尽量精简，在保证视觉效果的情况下选择最小的图片格式和图片质量，文件大小建议不要超过200K。使用图片地图使用（map），CSS Sprites等技术，尽量减少HTTP请求数。


## 书写规范
1. 开发过程中严格按分工完成页面，以提高css、js的复用率，避免重复开发。
2. 书写时，利用IDE工具实现层次分明的缩进。
3. 减少冗余代码，书写所有人都可以看的懂的代码。
4. 编写代码时注意SEO(搜索引擎优化)。比如`<img/>`添加alt属性，logo部分使用H1等

## HTML规范
### 模板

### 代码块
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="utf-8">
    <meta name="renderer" content="webkit|ie-comp|ie-stand">
    <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
    <meta name="keywords" content="">
    <meta name="description" content="">
    <title>标题内容</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<script src="common.js"></script>
</body>
</html>
```
### 原则
> 1. 规范：保证您的代码规范，趋html5,远xhtml，保证结构表现行为相互分离。
> 2. 简洁：保证代码的最简化，避免多余的空格、空行，保持代码的语义化，尽量使用具有语义的元素，避免使用样式属性和行为属性。任何时候都要用尽量简单、尽量少的元素解决问题。
> 3. 实用：遵循标准，但是不能以牺牲实用性为代价。
> 4. 忠诚：选择一套规范，然后始终遵循。不管代码由多少人参与，都应该看起来像一个人写的一样。

### 文档
> 1. 文档类型使用html5标准文档类型，文档类型声明之前，不允许出现任何非空字符。不允许添加`<meta>`强制改变文档模式。
> 2. html元素上指定lang属性。显示页面语言，有助于语言合成工具来确定怎样发音，以及翻译工具决定使用的规则，等等。
> 3. 指定明确的字符编码。让浏览器轻松、快速的确定适合网页内容的渲染方式。且与文件本身编码保持一致，统一使用推荐使用UTF-8编码`<meta charset="utf-8"/>`。
> 4. 根据页面内容和需求填写适当的`keywords`和`description`。
> 5. IE兼容模式。Internet Explorer 支持使用兼容性 `<meta>`标签来指定使用什么版本的 IE 来渲染页面。如果不是特殊需要，通常通过 edge mode 来通知 IE 使用最新的兼容模式。
> 6. 页面 `title `是极为重要的一项，不可缺少。控制在25个字、50个字节以内。
> 7. head部分的顺序： 
 > a. `<meta>`元素
 > b. 需要的js文件
 > c. `<title>`元素
 > d. 样式表
>8. 可以使用IE条件注释的方式兼容IE，但是不要添加额外的样式表
>9. 使用script将js文件引入，并置于body底部

### 格式
>1. 每一行都使用Tab缩进对齐,删除冗余的行尾的空格。
>2. 树形嵌套缩进。要有正确的层次，排版有规律工整。
>3. 块元素、列表元素、表格元素都放在新行。
>4. inline元素视情况换行。
>5. 努力保持每行长度小于80列，如果太长可换行。
>6. 模块之间必须保持独立，区块化布局，方便随意增删改，多人协作维护。
>7. 可以在大的模块之间用空行隔开，使模块更清晰。

### 元素
>1. 避免冗余标签，尽量遵循HTML标准和语义，但是不要以牺牲实用性为代价。任何时候都要尽量使用最少的标签并保持最小的复杂度。
>2. 语义化html，如标题根据重要性用h（同一个页面中只能有一个h1），段落标记用p，列表用ul，内联元素中不可嵌套块级元素等。
>3. 表现与结构完全分离，代码中最好不涉及任何的表现元素，如style、font、bgColor、border等。
>4. 列表项放`<ul>`、`<ol>`、`<dl>`，不要使用一系列的`<div>`或`<p>`
>5. `<input type="checkbox"/>`,'<input type="radio"/>'使用for属性绑定`<label>`。
>6. form button应制定`type`类型，使用`type="submit"`、`type="reset"`或`type="button"`。
>7. 有效使用`<thead>`、`<tfoot>`、`<tbody>`、`<th>`（scope属性）。可以把`<tfoot>`放`<tbody>`前提高加载速度。
>8. 特殊符号尽可能使用代码替代。常用特殊符号如下。
>- ¥：`&yen;` 人民币符号元
>- ©：`&copy;` 版权
>- ®： `&reg;` 注册商标
>- ™： `&trade;`商标TM
>- ·： `&middot;` 间隔符号
>- “： `&quot;` 双引号
>- &： `&amp;` &符
>- <： `&lt;` 小于号
>- `>`： `&gt;` 大于号
>- ： `&nbsp;` 半角空格
>- ×：`&times;` 乘号
>- ÷： `&divide;` 除号

>9. 样式都用class而不用id。原因如下： 
>-  id不可以重复，所以用class的话，可以肆无忌惮的用无数次。
>- id的优先级太高。
>- id专门留给JS用，用来标识行为。格式'js-*'。并且不要将此用于定义样式，不要包含在CSS文件中。

```
js-head
js-head_01
js-head_user
```

>10. class命名规则如下：
>- 只能出现小写字符、数字和破折号。
>- 名称应该尽可能短，并且意义明确（使用英文，不要使用汉语拼音缩写），避免过度任意的简写。
>- 基于最近的父class或者基本（base）class作为新class的前缀，在class中体现出层级关系。
>- 如果对相同class元素添加行为，格式'f-*'，并且不要将此用于定义样式，不要包含在css文件中。

> 常用命名
>- `wrapper`：页面外围控制整体布局宽度
>- `container`、`content`：容器用于最外层
>- `layout`：布局
>- `head`、`header`：页头部分
>- `foot`、`footer`：页脚部分
>- `nav`：主导航
>- `subnav`：二级导航
>- `topnav`：顶部导航
>- `menu`：菜单
>- `submenu`：二级菜单
>- `banner`：广告
>- `sidebar`：侧边栏
>- `main`：页面主体
>- `tag`：标签
>- `msg`：提示信息
>- `tips`：小技巧
>- `intro`：介绍
>- `note`：注释
>- `vote`：投票
>- `friendlink`：友情链接
>- `title`：标题
>- `summary`：摘要
>- `login`：登录
>- `register`：注册
>- `search`：搜索
>- `hot`：热门、热点
>- `copyright`：版权信息
>- `brand`：品牌、商标
>- `logo`：LOGO标志
>- `joinus`：加入我们
>- `partner`：合作伙伴
>- `service`：服务
>- `download`：下载
>- `arrow`：箭头
>- `icon`：图标
>- `guide`：指导、指南
>- `news`：新闻
>- `notice`：公告
>- `map`：地图
>- `group`：团购
>- `list`：列表
>- `item`：条目
>- `drop`：下拉
>- `scroll`：滚动
>- `tab`：标签页
>- `*-lt`：居左
>- `*-rt`：居右
>- `*-ct`、`*-md`：居中
>- `*-top`：顶部
>- `*-bt`：底部
>- `plus`：加
>- `minus`：减
>- `prev`：向前
>- `next`：向后

> 常用状态命名
>- `current`：当前
>- `hover`：悬停
>- `active`、`on`：激活状态
>- `disabled`：禁用状态
>- `selected`：已选择
>- `focus`：得到焦点
>- `blur`：失去焦点
>- `checked`：勾选
>- `success`：成功
>- `error`：错误

> 常用缩写模式
>- `btn`：button，按钮
>- `reg`：register，注册
>- `info`：information，信息
>- `li`：list，列表
>- `addr`：address，地址
>- `tel`：telphone，电话
>- `succ`：success，成功
>- `err`：error，错误
>- `bg`：background，背景

> 常用极简模式(浮动)
>- `fl`：left，用于左侧的部分、左浮动等
>- `fr`：right，用于右侧的部分、右浮动等
>- `cf`：清除浮动


### 属性
> 1. 所有标签名称和属性名称小写。
> 2. 双引号属性值，不要使用单引号。
> 3. 省略`type`属性。使用`style`、`link`、`script`，不用指定`type`属性，因为 `text/css` 和 `text/javascript` 分别是他们的默认值。
> 4. 省略Boolean属性值。Boolean属性不用添加取值，`disabled`，`checked`，`selected`等。
> 5. 属性顺序。html属性应该按照特定的顺序出现以保证易读性。 
> - a：`class `
> - b：`id`, `name`
> - c： `data-*`
> - d :  `src`, `for`, `type`, `href`
> - e： `title`, `alt`
> - f： `aria-*`, `role`

>6. 多媒体元素添加替代属性。图像增加alt属性，音视频增加替代文字。
>7. 不手动设置tabindex属性，让浏览器自动设置。

### 注释
>1. 详尽注释。解释代码解决问题、解决思路、是否为新鲜方案等。
>2. 给区块代码和重要功能加上注释，方便后台添加功能。
>3. 模块注释。github建议不使用模块结束注释。

```html
<!-----头部----->
<header></header>
……
<!-----尾部----->
<footer></footer>
```
**另外，请做到以下几点**

>1. 结构上如果可以并列书写，就不要嵌套。
如果可以写成`<div></div><div></div>`那么就不要写成`<div><div></div></div>`
>2. 如果结构已经可以满足视觉和语义的要求，那么就不要有额外的冗余的结构。
比如`<div><h2></h2></div>`已经能满足要求，那么就不要再写成`<div><div><h2></h2></div></div>`
>3. 一个标签上引用的className不要过多，越少越好。
比如不要出现这种情况：`<div class="class1 class2 class3 class4"></div>`

>4. 对于一个语义化的内部标签，应尽量避免使用className。
比如在这样一个列表中，li标签中的itm应去除：`<ul class="m-help"><li class="itm"></li><li class="itm"></li></ul>`

## CSS规范
### 文档
>1. 编码必须使用utf-8（无BOM）.CSS文件第一行声明该CSS文件的编码@charset "utf-8";。
>2. WEB端代码应能兼容主流浏览器，包括最新的火狐浏览器、谷歌浏览器、IE7-11等。允许不同的浏览器自带特性细微的差别。目前根据公司需求，针对低于内核IE9的浏览器采用提示用户升级操作，程序编写尽可能多采用H5，CSS3(浏览器内核注意)。
>3. 所有声明语句均以分号结尾。
>4. 分模块开发，修改模块时不能影响到其他部分样式，编写自适应的代码（eg：使用浮动之后要清除浮动、尽量不要定义固定高度、不要使用数值很大的margin和padding等）。
>5. 不要使用 `@import`。

### 选择器
>1. CSS选择器规范如下：
>- 对于通用元素使用class，这样有利于渲染性能的优化。
>- 对于经常出现的组件，避免使用属性选择器。
>- 选择器要尽可能短，并且尽量限制组成选择器的元素个数，建议不要超过3个。
>- 只有在必要的时候才将class限制在最近的父元素内（也就是后代选择器）。
>- 避免非必要的嵌套。



**不推荐**
```css
.reg-f{width:1000px;margin:0 auto;}
.reg-f1{background:#f8f8f8;}

.reg-f  .reg-f-h{line-height:30px;text-indent:20px;background:#ff2900;}
.reg-f  .reg-f-d{padding:20px 0;font-size:14px;}

.reg-f1 .reg-f1-li{float:left;width:250px;margin:0 20px;}
```
**推荐**
```css
.reg-f{width:1000px;margin:0 auto;}
.reg-f1{background:#f8f8f8;}

.reg-f-h{line-height:30px;text-indent:20px;background:#ff2900;}
.reg-f-d{padding:20px 0;font-size:14px;}

.reg-f1-li{float:left;width:250px;margin:0 20px;}
```

>2. 为选择器分组时，将单独的选择器单独放在一行。
>3. 不同选择器定义相同样式时，在后面添加一个空格，选择器较长时，换行显示。

**不推荐**
```css
.chip .list-l,.chip .list-r{border-top:1px solid #7ec15c;}
.youdao-banner .entry-reg input[type="text"], .youdao-banner .entry-reg input[type="password"], .youku-banner .entry-reg input[type="text"], .youku-banner .entry-reg input[type="password"]{background-color:#fff;}
```
**推荐**
```css
.chip .list-l, .chip .list-r{border-top:1px solid #7ec15c;}
.youdao-banner .entry-reg input[type="text"],
.youdao-banner .entry-reg input[type="password"],
.youku-banner .entry-reg input[type="text"],
.youku-banner .entry-reg input[type="password"]{background-color:#fff;}
```
>4. 媒体查询（Media query）放在尽可能相关规则的附近。

### 属性
>1. 属性名和十六进制值应该全部小写。
>2. 尽量使用简写形式的十六进制值。eg：`#fff`代替 `#ffffff` 。
>3. 为选择器中的属性添加单引号。eg：`input[type='text']`。
>4. 为引用的图片、文件等添加单引号。eg：`background:url('../images/logo.png')`;
>5. 避免为0值指定单位。eg：`margin:0`; 代替 `margin:0px`。
>6. `margin`和`padding`等属性，使用1个、2个或者4个属性值的写法，尽量做到缩写。eg：`padding:10px`;、`margin:0 auto`;、`padding:10px 15px 20px 10px`;
>7. 设置字体时，禁止使用中文，用相应的英文代替或者编码转换。eg：
>- 宋体（`SimSun`或者`\5b8b\4f53`）
>- 微软雅黑（`Microsoft YaHei`或者`\5FAE\8F6F\96C5\9ED1`）
>- 黑体（`SimHei`或者`\9ED1\4F53`）
>- 新宋体（`NSimSun`或者`\65b0\5b8b\4f53`）

>8. `background`按照color、image、repeat、position的顺序书写。并尽量做到简写
>9. 属性写在一行内，属性之间、属性名和值之间以及属性与“{}”之间应减少空格，eg：`.class{width:200px;height:100px}`
>10. 按照元素模型由外及内，由整体到细节书写。相关的属性声明应该归为一组，并按照下面的顺序排列： 
>- 显示属性：``display``,``list-style``,``position``,``float``,``clear`` …
>- 自身属性（盒模型）：``width``,``height``,``margin``,``padding``,``border`` 
>- 背景：``background``
>- 文本属性：``color``,``font``,``text-decoration``,``text-align``,``text-indent``,``vertical-align``,``line-height ``,``white-space``,``content``…  
>- 其他：``cursor``,``z-index``,``zoom``,``overflow``
>- CSS3属性或者其他：``transform``,``transition``,``animation``,``box-shadow``,``border-radius``  

>11. 针对特殊浏览器的属性，应写在标准属性之前，eg：`-webkit-box-shadow:;-moz-box-shadow:;box-shaow:;`
>12. 带有前缀的属性，单独一行，通过缩进，让每个属性的值垂直对齐，方便编辑维护。
>13. 尽量避免使用css表达式。eg：`background-color:expresssion((new Date()).getHours()%2 ? "#b8d4ff" : "#f08a00");`
>14. 慎用`!important`。
>15. 按标准写css，再针对特定浏览器作hack。尽量避免hack。
>16. css hack
>- IE6 :  ``_``
>- IE6/7 : ``*``
>- IE7 :  ``*+``
>- IE6/7/8 :  ``\9``
>- IE8 :  ``\0``

>17. 条件hack 
>- IE7以下版本：``<!--[if lt IE 7]><html class="no-js lt-ie9 lt-ie8 lt-ie7"><![endif]-->``
>- IE7：``<!--[if IE 7]><html class="no-js lt-ie9 lt-ie8"><![endif]-->``
>- IE8：``<!--[if IE 8]> <html class="no-js lt-ie9"><![endif]-->``
>- IE8以上：``<!--[if gt IE 8]><!--><html class="no-js"><!--<![endif]-->``



### 注释
1.css顶部注释
```css
/*
name:  文件的名称
@description: 简要的描述这个css 文件功能
@require: 依赖文件，没有就不用写
@author: 作者  最好附带联系方式(邮箱)
*/
```
2.确保你的代码能够自描述、注释良好并且易于他人理解。对于较长的注释，务必书写完整的句子；对于一般性注解，可以书写简洁的短语。

3.以组件为单位组织代码段。在相应组件上面添加多行注释，每个组件下面留出3行空白。注释格式如下
```css
/**
 * title
 * description
 **/
```



## Javascript规范
### 基本要求
>1. 每行代码结束必须有分号。
>2. 注重与html分离，减少reflow，注重性能。
>3. 代码结构明了，加适量单行或多行注释，提高函数重用率。
>4. 避免使用全局命名，导致空间污染，将代码包裹成一个 IIFE(Immediately-Invoked Function Expression)，用以创建独立隔绝的定义域。
>5. 切勿在循环中创建函数,在简单的循环语句中加入函数是非常容易形成闭包而带来隐患的

**不推荐**
```js
var x = 10,
    y = 100;
console.log(window.x + ' ' + window.y);
```
**推荐**
```js
 (function(log, w, undefined){
  'use strict';
  var x = 10,
      y = 100;
  log((w.x === undefined) + ' ' + (w.y === undefined));
}(window.console.log, window));
```

>6. 建议在自己的写的js文件中使用严格模式，即在最顶部添加`use strict`。启用严格模式，最好是在独立的 IIFE 中应用它，避免对其他插件报错。
>7. 尽量不要使用 evil 函数
>8. 首选函数式风格，简化代码并缩减维护成本并且它容易复用。
>9. 代码中不要出现大篇幅的空白换行，除非在用以区分功能块使用空白换行，其他地方不要使用
>10. 代码结构必须遵循“少，快，好”的原则，用最少的代码，执行最快的处理，做最好的程序；能够长久使用，重复使用，bug少。

**不推荐**
```js
(function(log){
  'use strict';
  var arr = [10, 3, 7, 9, 100, 20],
      sum = 0,
      i;
  for(i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  log('The sum of array ' + arr + ' is: ' + sum);
}(window.console.log));
```
**推荐**
```js
(function(log){
  'use strict';
  var arr = [10, 3, 7, 9, 100, 20];
  var sum = arr.reduce(function(prevValue, currentValue) {
    return prevValue + currentValue;
  }, 0);
  log('The sum of array ' + arr + ' is: ' + sum);
}(window.console.log));
```
>9. 建议使用 ES5 中新增的语法糖和函数。这将简化你的程序，并让你的代码更加灵活和可复用。(ES6里新添的函数和语法请在确定兼容性后再使用)
>10. 统一使用单引号(‘)，不使用双引号(“)。这在创建 HTML 字符串非常有好处：
>11. 用三元操作符分配或返回语句。在比较简单的情况下使用，避免在复杂的情况下使用。没人愿意用 10 行三元操作符把自己的脑子绕晕。
>12. 在使用插件时尽可能引用压缩后的文件。
>13. 不起渲染页面作用的只处理行为操作或者功能操作的js写在<body/>最底部

### 命名规范
**变量命名**

标准变量采用驼峰式命名
- ID在变量名中全大写
- URL在变量名中全大写
- Android在变量名中大写第一个字母
- iOS在变量名中小写第一个，大写后两个字母
- 常量全大写，用下划线连接
- 构造函数，大写第一个字母
- jquery对象必须以$开头命名

```js
var thisIsMyName;

var goodID;

var reportURL;

var AndroidVersion;

var iOSVersion;

var MAX_COUNT = 10;

function Person(name) {
    this.name = name;
}

var $body = $('body');
```
**前缀规范**

- s：表示字符串。例如：sName，sHtml;
- n：表示数字。例如：nPage，nTotal;
- b：表示逻辑。例如：bChecked，bHasLogin;
- a：表示数组。例如：aList，aGroup;
- r：表示正则表达式。例如：rDomain，rEmail;
- f：表示函数。例如：fGetHtml，fInit;
- o：表示以上未涉及到的其他对象，例如：oButton，oDate;


**函数命名**
1. 统一使用动词或者动词[+名词]形式，例如：fGetVersion()，fSubmitForm()，fInit();涉及返回逻辑值的函数可以使用is，has等表示逻辑的词语代替动词。
2. 如果有内部函数，使用__f+动词[+名词]形式，内部函数必需在函数最后定义。
3. 对象方法命名使用 f+对象类名+动词[+名词]形式;例如 fAddressGetEmail
4. 某事件响应函数命名方式为触发事件对象名+事件名或者模块名+触发事件对象名+事件名，例如：fDivClick()，fAddressSubmitButtonClick() 简写成fAddrSbtnClick()

**其它注意事项**

- 所有命名最好使用英语表示。
- 所有变量名应该明确而必要，尽量避免不必要的容易混淆的缩写。
- 对应的方法应该使用对应的动词，例如：get/set, add/remove, create/destroy, start/stop, insert/delete, begin/end。
- 应该避免双重否定意义的变量，例如：bIsNotError, bIsNotFound，不可取。
- 变量应该在最小的范围内定义，并尽可能的保持最少的活动时间。
- 循环变量最好在循环中定义。例如for(var i=0,m=10;i++)
- 尽量避免复杂的条件语句，可以使用临时的boolean变量代替。
- 一定要避免在条件中执行语句，例如：if((i=3)>2){}，不可取。
- 不要在代码中重复使用相同意义的数字，用一个变量代替

### 注释
我们可以添加注释来对 JavaScript 进行解释，或者提高代码的可读性。
- 单行注释以 // 开头。
- 多行注释以 /* 开始，以 */ 结尾。
- js文件开头需要注释文件的用途说明，参数，作者和日期等，格式;尤其在编写插件js文件，必须写好参数描述
- 函数和功能模块创建之前用注释好，一方面便于阅读，另一方面也起到的区分功能模块的作用

```js
  /**
    * 函数功能简述
    * 具体描述一些细节
    * @param {string} address 地址
    * @param {array} com 商品分组
    * @returns void
    *
    * date: 2016-03-11
    * author: liujian<liuj@3658mall.com>
    **/
```
- js中间函数和功能模块说明，以区分功能模块可使用下面两种格式

**需要详细的参数说明的**

```js
/**
* 翻转一个字符串
*
* @param  {String} 输入需要翻转的字符串
* @return {String} 翻转后的字符串
**/
```
**直接说明一下**
```js
/* 翻转一个字符串 */
/* ================================================== */
```
