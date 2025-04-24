# 东北大学秦皇岛分校（NEUQ）2025年本科毕业论文 LaTex 模板

本模板基于学长`onsimplet`的模板[NEUQPaperLatexTemplateUpdate](https://github.com/onsimplet/NEUQPaperLaTeXTemplateUpdate)修改优化，同时感谢学长 `coffin`的模板[PaperLatexTemplate](https://github.com/techflowing/PaperLaTexTemplate)与学长`happylzyy`的模板[NEUQPaperLatexTemplate](https://github.com/happylzyy/NEUQPaperLatexTemplate.git)

默认用户了解基本Latex指令，请在使用前安装所需环境并简单学习
OverLeaf上会提示字体缺失，暂未解决，需手动附带字体上传，并修改相关指令

后续遇到文档样式相关问题请在issue提及，我会第一时间查看，不解决Latex环境问题

## LaTeX环境

Windows11 系统下的VSCode和Texlive-2025，使用xelatex->bibtex->xelatex*2编译链
关于如何安装Texlive，请参考[TeX Live on Windows](https://tug.org/texlive/windows.html)
关于如何配置VSC下的Latex环境，请参考[VScode写LaTeX配置，实测有效](https://blog.csdn.net/BO_S__/article/details/136129261)
> 万物皆可VSCode

## 自定义命令

- 添加附录

```tex
\newcommand{\specialsection}[1]{% 正文后诸如“致谢”之类的章节，解决超链接问题
  \phantomsection
  \addcontentsline{toc}{section*}{\heiti\zihao{-4}#1}
  \section*{#1}
}

%使用例
\specialsection{附\ \ \ \ \ \ \ \ 录}


```

- 添加图片

```tex
\newcommand{\addimage}[4]{ % 添加图片 #1为宽度 #2为图片路径 #3为图片标题 #4为图片标签
  \begin{figure}[H]
    \centering
    \includegraphics[width=#1\textwidth]{#2}
    \caption{\ \ #3}\label{#4}
    \vspace{-1em}
  \end{figure}
}

%使用例
\addimage{0.1~1}{图片路径}{图片标题}{fig:something}

```
其他待更新

---
以下为原模板部分README

## tips

* 毕设封面是参照word模板制作的，与word模板的有些不同，可以自行修改或者单独将word模板封面导出PDF版添加引用。
* 参考文献样式为GB/T 7714-2005，所支持的硕士学位论文参考文献标识在bibtex文件中是masterthesis，而不是mastersthesis。

## 参考资料

* [LaTeX 里「添加程序代码」的完美解决方案](https://zhuanlan.zhihu.com/p/65441079)
* [设置Latex页眉页脚边距——fancyhdr的使用](https://blog.csdn.net/SStegosaurus/article/details/105013643)
* [latex中如何做像填空题那样的下划线？](https://www.zhihu.com/question/25259266?sort=created)
* [LaTeX使用笔记：长表格longtable（附实例）](http://sparkandshine.net/latex-use-notes-longtable-with-examples/)
