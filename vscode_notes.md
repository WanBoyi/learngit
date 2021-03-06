## 1. VS 简介

VS 是代码编辑器（文本编辑器+IDE），但是集成了许多的插件，可以通过插件快速实现一些功能，非常的简洁轻便

有**跨平台，免费**的特点
优点如下：

1. 轻量级：相比起 VS 的臃肿，VS 打开文件的速度非常快，也不用庞大的项目文件，使用工作区的机制，方便文件的管理
2. 占用开销小：不论是占用内存大小还是软件的安装容量，都非常适合使用，没有复杂的安装过程，小白可以轻松配置，程序员也可调整开发环境
3. 功能强大且易用：通过 github 上火爆的开源插件，可以实现一些复杂的 IDE 才能实现的功能，不仅保持了功能的完整性，同时也符合精简的要求
4. 内部集成 Git：方便使用版本管理，这个学习了再说
5. 界面美观：用 vs 编写 md 文件是真的省心，预览的排版也比浏览器的舒服很多
6. 跨平台使用：win，mac，linux

## 2. 界面与布局

使用左右分屏，有两种适用场合

1. 编写 markdown 文件，同步观看预览，调整排版
2. 两个文件进行对比（Mac 有个快捷键 command+鼠标点击）没太用过，先留个坑

## 3. 常用快捷键
//TODO:Mark 一下，留个坑回来填

## 4. 代码编辑小工具

#### 1. 双击文字，自动高亮其他文字

可以快速找到相同的变量名的位置

#### 2. 通过插件使用其他的主题和字体

比如现在使用的黑夜主题，字体也可以安装调整，md真的太舒服了，吹爆vscode

#### 3. 显示不可见的控制字符

> Code->首选项->Settings->搜 editor.renderControlCharacters ->
> 勾选：Editor: Render Control Characters 中的 Controls whether the editor should render control characters
> 可以显示特殊的不可见的字符

#### 4. 设置 tab 的宽度=n 个空格的个数

具体查一下，代码一般是 n=4，文字一般是 n=2

## 5. 使用终端（啥是终端，啥时候用）

先区分几个小的概念吧

命令行：比如 windows 里面的 cmd，linux 里的 bash，通过输入命令进行操作的

终端(Terminal)=输入设备+输出设备,即终端不包含 CPU 和存储器以及软件

控制台(console)是一种特殊的终端，一台机器可由有多个终端，但只能有一个控制台供管理员使用

shell(壳层)提供了用户操作系统的入口，其中命令行 shell 有 cmd 和 bash

//TODO:如何使用终端，何时使用终端在这留个坑

## 6. 代码格式化
先设置文件的格式（比如要设置为json），再右键格式化，就会高亮缩进

## 7. 文件编码
将文件在vs中打开，可以自动检测到编码格式
并且可以在文件的保存时选择一个文件编码
**语言模式与文件编码都在最底下那行**

## 8. 语法高亮
当设置了文件的后缀名格式时，一般内置的会语法高亮，包括html和log文件等，如果没有可以自己下载插件实现

## 9. 搜索与替换
可以在当前文件，也可以在整个项目内，进行搜索与替换
（正则搜索与替换？？？留坑）

## 10. 查找函数定义
在Mac里面，把鼠标放到函数名上
>command+鼠标点击
可以赚到函数的定义上去

## 11. 快速跳转文件
>command+p
然后输入文件名，选择文件后回车
即可直接跳转文件

## 12. 通过log跳转文件
在多个文件的大项目中，如果调试出错，点击日志中的文件路径，可以直接跳转打开该文件

## 13. 大纲跳转
大纲有两处，一个是顶部，包含了文件路径和大纲（也可以在顶部的文件路径选择打开文件）还有文件侧边栏的大纲

## 14. Git管理代码仓库
新增的行用绿线标出，删除的行用红线标出
改变的行用蓝线标出，md真的舒服

先用git bash简历代码仓库，然后在仓库内创建.md文件，在bash中通过git add加入该文件，然后就非常方便修改了

这里的暂存add与提交commit都直接用界面图标即可操作，记得每次提交要写备注，这点真的很贴心

如果要查看提交的记录历史，一个方法是在git bash中查看，一个是在vscode中安装插件git history

这tm也太好用了吧！爱了爱了，舒服的一批

## 15. 集成终端
集成终端是为了不用切换到外部的终端命令行，只在一个界面内就完成不同事物的处理

比如可以在终端内完成git bash的功能，也可以在终端内完成MySQL的命令行功能

非常方便 但留个坑···

## 16. 一些好用的插件
paste image：用于快速粘贴图片
···

## 17. 用vs写python、
vs写python是相当不错的环境，以后可以试试






