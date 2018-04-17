==========================
Html5 + CSS3 CheatSheet整理
==========================

Html5和Css3是万维网标准通用标记语言下的一个应用超文本标记语言的第5次修改，相比于html4增添了许多新特性。整理了一些常用的东西，希望能帮助大家。

**参考资料**

[小P分享的链接]http://www.simplehtmlguide.com/cheatsheet.php

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
- <ul> <li> 列表 </li> </ul> 无需列表，前面是圆点
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

- <span> ... </span>  文字内容划分 ::

		span属于块元素，如果想对span内的文字进行样式设置，比如对齐方式的设置，
		需要添加display：block将其转化为块元素，否则对齐设置无法生效。

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

- <table> ... </table> 定义表格
- <table> 属性::

    - border="?"  外边框宽度
    - bordercolor="#??????"   边框颜色
    - cellspacing="?" 单元格见空隙(像素)
    - cellpadding="?" 单元格与内容间的空间
    - align="??" 对齐方式（left, center, right）
    - bgcolor="#??????" 表格背景颜色
    - width="??"  表格宽度(像素或百分比)
    - height="??" 表格高度 (像素或百分比)

- <tr> ... </tr>  列
- <th> ... </th>  列标题
- <td> ... </td>  列内单元格
- <td> 属性::

    - colspan="?" 行单元格合并数量 (合并单元格)
    - rowspan="?" 列单元格合并数量 (合并单元格)
    - width="??"  单元格宽度 (像素或百分比) (*)
    - height="??" 单元格高度 (像素或百分比) (*)
    - bgcolor="#??????"   单元格颜色设置 (*)
    - align="??"  水平对齐方式（左中右）
    - valign="??" 垂直对齐方式（上中下）
    - nowrap  在单元格内强制不换行


表单
----

- <form> ... </form>  定义form表单
- <form> 属性值::  

    - action="url"    规定当提交表单时，向何处发送表单数据
    - method="***"    规定如何发送表单: get, post

- <input> ... </input>   输入框
- <input> 属性::  

    - type="***"  输入框类型（text, password, checkbox, submit etc）
    - name="***"  规定input的名称，方便后期数据引用 
    - value="***" 输入框的值
    - size="***"  输入框大小
    - maxlength="?"  输入数据的最大长度
    - checked   标记选中的组合按钮和复选框

- <select> ... </select>  下拉选择表单
- <select> 属性值::    

    - name="***"  下拉菜单名称，方便后期数据引用
    - size="?"    选项个数
    - multiple    允许多选

- <option> ... </option>  在下拉列表里选择
- <option> 属性::

    - value="***" 选择值
    - selected    设置默认选择

- <textarea> ... </textarea> 文本域
- <textarea> 属性值::

    - name="***"  文本域名称，方便后期数据引用
    - rows="?"    文本域内可见行数
    - cols="?"    规定文本区的宽度（字符个数）
    - wrap="***"  规定当在表单中提交时，文本区域中的文本如何换行（hard|soft）
    - required 必填项


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

    CSS优先级：行内 > 内部引用 > 外部引用。
    当在一个样式声明中使用一个!important 规则时，此声明将覆盖任何其他声明。
    另外，CSS中也有样式继承的概念。

相信大家应该都知道了css选择器的概念并会使用了。下面就整理一些常用的样式设置。

CSS在使用的时候有一个通用布局（全局）和局部布局的概念。

#. 通用布局：在整个项目中都会用到且一般不会在项目中进行样式更改的。这些样式设置我们一般会放在css文件的最顶部。
#. 局部布局：单个元素或单个标签或者单个页面文件都可以单独设置其属性。

颜色和边框样式
-----------

- color: red; 元素颜色，值可以是（red|#FF0000）
- background-color: white;  背景颜色
- background-image: url(image.gif); 背景图片
- border-color: yellow; 边框颜色
- border: 1px solid blue; 边框宽度、样式和颜色（都有其他值可选）
- border-radius: 5px; 圆角边框

.. note::

	color颜色的值，可以使red和#xxxx以及rgb(255,255,255)这三种形式。
	
	区别：
		red、blue、green等表示颜色的单词作为值时，等同于三个特定的#xxxxxx值。
		
		#xxxxxx和rgb(255,255,255)这两种形式的值可以表示色板中任意颜色值。
		
		另外还有一种颜色表示方法，rgba，其中a是alpha表示透明度
		
		样例：color：rgba(0,0,0,0.1)表示透明度为0.1的黑色。大家可以手动试一下。


文字样式设置
----------

- text-align: left; 文字对齐方式，值（left | center | right）
- text-decoration: underline; 字体装饰（none|underline |line-through）
- font-family: fontname;  字族（如：微软雅黑，Verdana, Arial, Helvetica）
- font-size: 16pt;  字体大小（可用磅和像素表示，如12pt | 15px）
- font-weight: bold; 字体粗细（值：bold | normal | 200） 

大小和布局
--------
- width: 400px; 宽度（像素或百分比）
- height: 100%; 高度（像素或百分比）
- margin: 5px; 元素外边距（可一次设置4个值，如：margin: 5px 4px 6px 7px - 位置对应 上右下左 顺时针边距）
- margin-top: 1px; 元素之间上边距
- padding: 5px; 块元素内部边距，用法与margin类似
- padding-top: 1px; 

CSS列表
------
- list-style: none; 列表样式（无圆点等装饰）