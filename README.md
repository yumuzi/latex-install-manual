# Windows 7 x86/x64 安装LaTeX教程

本文章仅教如何将 latex 安装在 Windows 7 系统中，并且可以使用 UTF-8 中文编码（即编好的PDF文档可以收录中文）。对于如何使用 latex 编辑论文请参考相关 latex 书籍、Google 或参考相关文献。



## 1. 安装 MikTex 2.9

* 软件下载网址：[MikTex 2.9](http://miktex.org/download)

* 32-bit/64-bit 择一下载并安装。



## 2. 更新 MiKTex

* 安装完 MikTex 之后到

    开始 -> 所有程序 -> MikTex 2.9 -> Maintenance(Admin) -> MikTex Update(Admin)

  点开后选择（默认即可）：

	I want to get updated packages from a remote package repository

  执行下一步，搜索完后选择全选执行下一步，等待更新完成即可。如果没有搜素到更新就可以直接关掉程序。

  

## 3. 为 MikTex 安装xeCJK 套件（UTF-8编码用）

* 进入到


	开始 -> 所有程序 -> MikTex 2.9 -> Maintenance(Admin)   -> MikTex Package Manager(Admin)

  在“name”中搜索“xe”，并全部安装。

  

## 4. 安装编译器 Texmaker

* 软件下载地址：[Texmaker 4.5 for Windows](http://www.xm1math.net/texmaker/download.html)，32-bit/64-bit通用。



## 5. Texmaker 配置

> 安装完成后，执行 Texmaker

	选项 -> 配置 Texmaker

 左边有四个选项，需分别对命令、快速构建和编辑器进行配置：

> > 1. 命令：

> > > * (1.1) 第一项 LaTeX 中加入"xe"，变为:xelatex -interaction=nonstopmode %.tex

> > > * (1.2) Pdf查看器更改为"External Viewer"（即你的电脑上安装的PDF阅读软件），举例:"D:/Program Files (x86)/Foxit Software/Foxit PhantomPDF/Foxit PhantomPDF.exe" %.pdf

> > 2. 快速构建：

> > > * 选择“用户”，将上述(1.1)+(1.2)填入空格内，中间以"|"分隔，最后结尾再补上"| bibtex %.aux|xdvi %.dvi"即可。举例:xelatex -interaction=nonstopmode %.tex | "D:\Program Files (x86)\Foxit Software\Foxit PhantomPDF\Foxit PhantomPDF.exe" %.pdf | bibtex %.aux|xdvi %.dvi

> > 3. 编辑器：

> > 编辑器 -> 编辑器字体编码 选择"UTF-8"


----

**完成以上配置即可开始使用latex！**
