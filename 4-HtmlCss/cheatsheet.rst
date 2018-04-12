==========================
Html5 + CSS3 CheatSheet整理
==========================

Html5和Css3是万维网标准通用标记语言下的一个应用超文本标记语言的第5次修改，相比于html4增添了许多新特性。整理了一些常用的东西，希望能帮助大家。
参考文婷发给的网址：http://www.simplehtmlguide.com/cheatsheet.php

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
#. 浏览至 *source* 文件夹，并在其根目录下创建新文件夹demo
#. 在上方 *demo* 文件夹中，新建test.rst文件，并在其中输入如下内容：

::

        =======================
        这是Sphinx的测试
        =======================
        我爱学习Sphinx




图片
----

#. 打开 *source* 文件夹中的conf.py，并找到主题配置行 html_theme = 'alabaster'
#. 从内置主题中挑选需要的主题，如 bizstyle，将其改为 html_theme = 'bizstyle'



链接
----

如果喜欢 `readthedocs.org <https://docs.readthedocs.io/en/latest/getting_started.html>`_ 的主题，可以按照如下方式安装

.. code-block:: python

    pip install sphinx_rtd_theme

安装之后，再按照上述步骤，将 ``conf.py`` 中的主题行，修改为html_theme = 'sphinx_rtd_theme'，再运行 ``sphinx-build`` 命令重新发布即可。

列表
----

执行 ``sphinx-build`` 命令后，sphinx会将rst的内容，发布为静态网站。只需将 *build* 文件夹中的文件，托管至github，即可实现公网访问。


Table表格
--------

每次更新后，都需执行 ``sphinx-build`` 命令，并重新上传至Github，较为麻烦。这个工作可以由ReadTheDocs平台自动化完成。


frame框架
--------

#. 注册ReadTheDocs账号
#. 将Github账号关联到ReadtheDocs
#. 将source文件中的内容，上传至github中的某个repo中


表单
----

#. 选择github的相应ropo，自动创建webhook
#. 后续每次源文件内容有变化后，ReadtheDoc均可以自动发布最新的版本


特殊符号
------

更多内容参见ReadtheDocs官方文档：https://docs.readthedocs.io/en/latest/getting_started.html


body背景及颜色设置
---------------

* reStructedText 
* 自定义主题
* 制作主题
* 发布为PDF等其他样式
 
预习：

* HTML，CSS
* Jinjia 模板语言

**参考资料**

[Sphinx官方教程]: http://www.sphinx-doc.org/en/master/usage/quickstart.html