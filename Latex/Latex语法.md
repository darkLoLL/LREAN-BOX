# Latex语法

## 基础形式

`\命令名{参数}`开始命令

## 文档类型

```latex
指定文档类型
\documentclass {article}
book, report等, 幻灯片 beamer
显示中文文档, 中英混排
\documentclass[UTF8]{ctexart}
```



## 前言 preamble

位于 `\begin{*document*}`之前的内容

## 正文

位于 `\begin{*document*}`和 `\end{*document*}`之间

## 标题 作者 日期

```latex
\title{loll的标题}
\author{dark loll}
\date{2023-6-16}

在中文中显示信息, 要添加命令
\maketitle
```

## 常用格式化

```latex
\textbf{加粗} \textit{斜体} \underline{下滑线标记文字}
```

## 章节(chapter and section)

```latex
\section{}
\subsection{}
```

`chapter`的使用

```latex
\documentclass[UTF8]{ctexbook}

\part*{第一部}
\chapter*{第一章}
```

## 图片

```latex
\documentclass[UTF8]{ctexbook}

% 导入
\usepackage{graphicx}

\begin{document}
\begin{figure}
    % 居中
    \centering
    \includegraphics[width=1\linewidth]{img/wlop.jpg}
    \caption{绯}
\end{figure}

\end{document} 
```

## 有序和无序列表

```latex
\documentclass[UTF8]{ctexart}

\begin{document}
无序列表

\begin{itemize}
    \item c
    \item cpp
    \item rust
\end{itemize}

有序列表

\begin{enumerate}
    \item python
    \item java
    \item going
    \item matlab
\end{enumerate}

\end{document} 
```

## 公式

```latex
\documentclass[UTF8]{ctexart}

\begin{document}
\textbf{行内公式} : $E=m*c^2$

\begin{equation}
    d={k \varphi(n) + 1} \over e
\end{equation}

\[
    F=ma  
\]

\end{document}
```

## 表格

```latex
\documentclass[UTF8]{ctexart}

\begin{document}
\begin{table}
    \center
    \begin{tabular}{| p{2cm} c c c |}
        \hline
            姓名 & 年龄 & 班级 & 备注 \\
            \hline
            Tim & 12 & 初一 & \\
            Marry & 11 & & over \\
        \hline
    \end{tabular}  
    \caption{记录} 
\end{table}
\end{document}
```

