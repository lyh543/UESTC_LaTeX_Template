# 电子科技大学计算机学院实验报告 LaTeX 模板

本模板基于[heywrcoding/UESTC_Lab_Report_LaTeX_Template]，参考[标准实验报告.doc]和[标准实验报告_multipart.doc]修改。

## 说明

计院模板千千万，其实也就是两个风格：**多次实验的内容合并为一个报告来写（[标准实验报告.doc]），或者每次实验写一个报告并标注明显的实验X （[标准实验报告_multipart.doc]）**。

对于这两个风格，可以分别使用 [main.pdf] 或 [main_multipart.pdf] 来完成。

[heywrcoding/UESTC_Lab_Report_LaTeX_Template]: https://github.com/heywrcoding/UESTC_Lab_Report_LaTeX_Template/
[标准实验报告.doc]: 标准实验报告.doc
[标准实验报告_multipart.doc]: 标准实验报告_multipart.doc
[main.pdf]: main.pdf
[main_multipart.pdf]:main_multipart.pdf

## 简易的使用手册

### 编译选项

使用 `xelatex` 编译。

在 Windows 10 (64 位)，TeXLive 2019 通过编译。

### 文字格式设置

#### 字体设置

使用 `\song{text}` 即可设置 `text` 的字体。其余字体见下表：

字体|命令
-|-
宋体|`\song`
仿宋|`\fs`
楷体|`\kaishu`
黑体|`\hei`
微软雅黑|`\yh`
华文行楷|`\hwxk`
方正舒体|`\fzshu`

#### 加粗设置

使用 `{\bfseries text}` 即可加粗 `text`。

#### 设置字号

使用 `\chuhao` 可设置为初号字体。更多字体如下。亦可使用 `\fontsize{size}{skip}` 的格式手动指定字体大小和行距。

```latex
\newcommand{\chuhao}{\fontsize{42bp}{63bp}\selectfont}     %初号， 1.5倍行距
\newcommand{\xiaochuhao}{\fontsize{36bp}{36bp}\selectfont} %小初号，单倍行距
\newcommand{\yihao}{\fontsize{26bp}{39bp}\selectfont}        % 一号, 1.5 倍行距
\newcommand{\erhao}{\fontsize{22bp}{33bp}\selectfont}        % 二号, 1.5倍行距
\newcommand{\xiaoerhao}{\fontsize{18bp}{18bp}\selectfont}       % 小二, 单倍行距
\newcommand{\sanhao}{\fontsize{16bp}{24bp}\selectfont}       % 三号, 1.5倍行距
\newcommand{\xiaosanhao}{\fontsize{15bp}{22bp}\selectfont}      % 小三, 1.5倍行距
\newcommand{\sihao}{\fontsize{14bp}{21bp}\selectfont}        % 四号, 1.5 倍行距
\newcommand{\banxiaosi}{\fontsize{13bp}{20bp}\selectfont}  % 半小四, 20pt行距
\newcommand{\xiaosihao}{\fontsize{12bp}{20bp}\selectfont}       % 小四, 20pt行距
\newcommand{\dawuhao}{\fontsize{11bp}{11bp}\selectfont}      % 大五号, 单倍行距
\newcommand{\wuhao}{\fontsize{10.5bp}{10.5bp}\selectfont}   % 五号, 单倍行距
\newcommand{\xiaowuhao}{\fontsize{9bp}{9bp}\selectfont}   %小五号，单倍行距
```

### 标号设置

支持以下命令：

* `\section{title}` 显示为 `一、title`
* `\subsection{title}` 显示为 `（一）title`
* `\begin{enumerate} \item \end{enumerate}`，并且支持嵌套
* `\begin{itemize} \item \end{itemize}`


### 插入图片

如下为插入 `/img/logo.png` 图片，并给予题注的方法。

```latex
\begin{figure}[!htbp]
\centering
\includegraphics[width=\textwidth]{logo}
\bottomcaption{\xiaowuhao{电子科技大学}}
\end{figure}
```

## 已知 bug

1. [main_multipart.tex] 的标题（电子科技大学 实验报告 实验X）上方存在大量空白。
