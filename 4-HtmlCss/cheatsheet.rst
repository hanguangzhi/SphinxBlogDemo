==========================
Html5 + CSS3 CheatSheet整理
==========================

Html5和Css3是万维网标准通用标记语言下的一个应用超文本标记语言的第5次修改，相比于html4增添了许多新特性。整理了一些常用的东西，希望能帮助大家。

**参考资料**

[文婷分享的链接]http://www.simplehtmlguide.com/cheatsheet.php

网页模版
=======

每个网页都包含html、head、title、meta和body元素。一般创建网页的前几行都是一样的:

::

    .. <!DOCTYPE html> //html5文档类型声明

        <html lang="en"> //语言设置

            <head>

                <title>html标题</title>

                <meta charset = "utf-8">编码格式

                <link rel= "stylesheet" type="text/css" href="css.css"/> 
                //如有css文件，可通过此语句引入使用。（链接路径可自行修改）

            </head>

            <body>

                body content

            </body>

        </html>


html部分
=======

常用标签(以下标签均为封闭标签)
------------------------
- <h?> 标题 </h?> h1-h6标题，从大到小
- <p> 段落 </p>  文章段落
- <b> 加粗 </b>   加粗字体
- <i> 斜体 </i> 
- <a href="url"> 链接 </a> 创建链接
- <div> 块 </div> 块布局
- <img src="filename.jpg">  展示图片
- <ul> <li> 列表 </li> </ul> 无需列表，前面是原点
- <br> 换行
- <span style="color:red"> red </span> 使用内置样式


文本格式
-------
- <b> 文本加粗 </b> 
- <i> 文本斜体 </i> 
- <u> 加下划线 </u> 
- <strike> 加删除线 </strike>
- <sup> 上角标</sup> 
- <sub> 下角标 </sub>
- <small> 呈现小号字体</small>
- <tt>定义打字机字体</tt>
- <pre>保留文本原格式</pre>
- <blockquote>块引用</blockquote>
- <strong>字体加粗</strong>
- <em>强调，显示为斜体</em>  Emphasis - Shown as Italics in most browsers
- <font>字体</font>可用css定义




块划分
-----
- <div> ... </div> ::
    
        定义文档中的分区或块或节，可以把文档分割为独立不同的部分。
        可以用id或class来定义标记，使得此标签更有效。
        但是也不必为每个div都加id或class

- <span> ... </span>  文字内容划分
- <p> ... </p>  文字段划分
- <br> 行划分（换行）
- <hr> 水平线 ::

    属性值     
    - size="?"  水平线像素厚度
    - width="?"  像素宽度
    - width="??%" 像素百分比
    - color="#??????" 颜色定义
    - align="?" 水平位置
    - 没有阴影、3D和切割属性
    - <nobr> ... </nobr> 线换行



图片IMG
------

- <img src="url" alt="text"> 图片基础属性
- <img> 标签属性 ::

    - src="url"   URL或图片名(必须)
    - alt="text"  可选文字 
    - align="?"   图片嵌入方式
    - width="??"  宽度 (像素或百分比)
    - height="??" 高度 (像素或百分比)
    - border="??" 边宽 (像素)



链接（锚元素）
----------

- <a href="url"> link text </a> 基础a标签
<a> 标签属性 ::

    - href="url"  链接指向url
    - name="??"   链接地址名称
    - target="?"  链接页面打开方式: _self当前页跳转, _blank新页面打开(常用的两种方式).
    - href="url#bookmark" 链接到#id位置(锚点定位).
    - href="mailto:email" 邮件发送

列表
----

- <ol> ... </ol>  有序列表
- <ul> ... </ul>  无序列表
- <li> ... </li>  列表元素（有序和无序）
- <ol type="?">   有序列表类型: A, a, I, i, 1
- <ol start="??"> 有序列表开始值
- <ul type="?">   无序列表类型: disc, circle, square
- <li value="??"> 列表值 (改变当前或子列表的值)
- <li type="??">  列表样式 (只改变当前item)
- <dl> ... </dl>  内容列表
- <dt> ... </dt>  定义的term或phrase
- <dd> ... </dd>  详细内容


Table表格
--------

- <table> ... </table>    Define a Table
- <table> Tag Attributes::

    - border="?"  Thickness of outside border
    - bordercolor="#??????"   Border Colour
    - cellspacing="?" Space between cells (pixels)
    - cellpadding="?" Space between cell wall and content
    - align="??"  Horizontal Alignment: left, center, right (*)
    - bgcolor="#??????"   Background Colour (*)
    - width="??"  Table Width (pixels or %) (*)
    - height="??" Table Height (pixels or %) (*)

- <tr> ... </tr>  Table Row within table
- <th> ... </th>  Header Cell within table row
- <td> ... </td>  Table Cell within table row
- <td> Tag Attributes::

    - colspan="?" Number of columns the cell spans across (cell merge)
    - rowspan="?" Number of row a cell spans across (cell merge)
    - width="??"  Cell Width (pixels or %) (*)
    - height="??" Cell Height (pixels or %) (*)
    - bgcolor="#??????"   Background Colour (*)
    - align="??"  Horizontal Alignment: left, center, right (*)
    - valign="??" Vertical Alignment: top, middle, bottom (*)
    nowrap  Force no line breaks in a particular cell


frame框架
--------

- <frameset> ... </frameset>  Define the set of Frames
- <frameset> Tag Attributes:   
- rows="??,??, ..."   Define row sizes & number of rows (size in pixels or %)
- cols="??,??, ..."   Define column sizes & number of columns (size in pixels or %)
- noresize="noresize" User cannot resize any frames in frameset
- <frame> ... </frame>    Define a frame within the frameset
- <frame> Tag Attributes:  
- src="url"   Location of HTML File for a frame
- name="***"  Unique name of frame window
- marginwidth="?" Horizontal margin spacing inside frame (pixels)
- marginheight="?"    Vertical margin spacing inside frame (pixels)
- noresize="noresize" Declare all frameset sizes as fixed
- scrolling="***" Can the user scroll inside the frame: yes, no, auto
- frameborder="?" Frame Border: (1=yes, 2=no)
- bordercolor="#??????"   Border Colour (*)
- <noframes> ... </noframes>  Unframed content (for browsers not supporting frames)


表单
----

- <form> ... </form>  Form input group decleration
- <form> Tag Attributes::  

    - action="url"    URL of Form Script
    - method="***"    Method of Form: get, post
    - enctype="***"   For File Upload: enctype="multipart/form-data"

- <input> ... </input>    Input field within form
- <input> Tag Attributes::  

    - type="***"  Input Field Type: text, password, checkbox, submit etc.
    - name="***"  Form Field Name (for form processing script)
    - value="***" Value of Input Field
    - size="***"  Field Size
    - maxlength="?"   Maximum Length of Input Field Data
    checked Mark selected field in radio button group or checkbox

- <select> ... </select>  Select options from drop down list
- <select> Tag Attributes::    

    - name="***"  Drop Down Combo-Box Name (for form processing script)
    - size="?"    Number of selectable options
    - multiple    Allow multiple selections

- <option> ... </option>  Option (item) within drop down list
- <option> Tag Attributes::

    - value="***" Option Value
    - selected    Set option as default selected option

- <textarea> ... </textarea>  Large area for text input
- <textarea> Tag Attributes::

    - name="***"  Text Area Name (for form processing script)
    - rows="?"    Number of rows of text shown
    - cols="?"    Number of columns (characters per rows)
    - wrap="***"  Word Wrapping: off, hard, soft


特殊符号
------
- &lt;  < 小于
- &gt;    > 大于
- &amp;   & 
- &quot;  " 
- &copy;  © 
- &trade; ™ 
- &nbsp;  空白


body背景及颜色设置
---------------

- <body> 属性值 ::

    - background="url"  背景图片 (*)
    - bgcolor="#??????"   背景颜色 (*)
    - text="#??????"  文字颜色 (*)
    - link="#??????"  未访问链接颜色 (*)
    - vlink="#??????" 已访问链接颜色 (*)
    - alink="#??????" 鼠标点击超链接时的颜色 (*)
    - bgproperties="fixed" 背景固定，不随鼠标滚动而变化
    - margin="?" 设置外边距（像素）
    - padding="?" 设置内边距（像素）


CSS部分
=======
层叠样式表(Cascading Style Sheets)是一种用来表现HTML或XML等文件样式的计算机语言。CSS不仅可以静态地修饰网页，还可以配合各种脚本语言动态地对网页各元素进行格式化。能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式编辑的能力。

使用方式（共4种，常用的为3种）
------------------------
#. 引入独立css文件方式::

    <head>
        <link rel="stylesheet" type="text/css" href="style.css" title="style">
    </head>

#. html内部引用方式::

    <head>
        <style type="text/css">
         h1 {
            color:red;
            }
        </style>
    </head>

#. html行内引用::

    <p style="color:red;">Some red text</p>

#. 引入外部样式表::

    @import url(sheet.css);
    引入css文件到当下css文件中，且只能引入css文件。@import只能位于文件的顶部


.. note:: 

    CSS优先级：行内 > 内部引用 > 外部引用
    当在一个样式声明中使用一个!important 规则时，此声明将覆盖任何其他声明。
    CSS中也有继承的概念。

相信大家应该都知道了css选择器的概念并会使用了。下面就整理一些常用的样式设置。

颜色和边框样式
-----------

- color: red; Element Colour - eg. red | #FF0000
- background-color: white;    Background Colour of element
- background-image: url(image.gif);   Background Colour of element
- border-color: yellow;   Border Colour of element
- border: 1px solid blue; Width, style and colour of border defined together

文字样式设置
----------

- text-align: left;   Horizontal Alignment - left | center | right
- text-decoration: underline; Text Decorations - eg. none | underline | line-through
- font-family: fontname;  Font Face (Typeface) - eg. Verdana, Arial, Helvetica
- font-size: 16pt;    Font Size or Height - eg. 12pt | 15px
- font-weight: bold;  Font Weight (Boldness) - eg. bold | normal | 200

大小和布局
--------
- width: 400px;   Width of HTML element - eg. 100px | 50%
- height: 100%;   Height of HTML element - eg. 20px | 100%
- margin: 5px;    Margin - space around an element, or distance between two elements
- margin-top: 1px;    Top Margin. Also try -bottom: -left: or -right:
- padding: 5px;   Padding - distance between an elements contents and its border
- padding-top: 1px;   Top Padding. Also try -bottom: -left: or -right:

CSS列表
------
- list-style: none;   Clear existing bullet types set by html list tags
- text-decoriation: none;