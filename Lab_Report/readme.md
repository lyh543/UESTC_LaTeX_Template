# 电子科技大学计算机学院实验报告 LaTeX 模板

本模板基于[heywrcoding/UESTC_Lab_Report_LaTeX_Template](https://github.com/heywrcoding/UESTC_Lab_Report_LaTeX_Template/)，参考[标准实验报告_模板.doc]修改，修改之处见[文末](#修改)。

[原项目的 README](https://github.com/heywrcoding/UESTC_Lab_Report_LaTeX_Template/blob/master/README.zh-CN.md)

[LaTeX 模板] [预览 pdf]

[LaTeX 模板]: https://github.com/lyh543/UESTC_LaTeX_Template/blob/master/Lab_Report/lab_report(zh-cn)/lab_report(zh_cn).tex
[标准实验报告_模板.doc]: https://github.com/lyh543/UESTC_LaTeX_Template/blob/master/Lab_Report/标准实验报告_模板.doc
[预览 pdf]: https://github.com/lyh543/UESTC_LaTeX_Template/blob/master/Lab_Report/lab_report(zh-cn)/lab_report(zh_cn).pdf

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

## 修改

1. 定义 `AutoFakeBold`，使用全局伪粗体，应对某些字体无法粗体的 bug。
2. 引入了方正舒体 `\fzshu`。
3. 针对电子科技大学计算机学院的实验报告模板对 section 的名称和顺序、字体、页脚和其他一些细节进行了修改。
