# 电子科技大学课程论文模板

基于 [x-magus/ThesisUESTC](https://github.com/x-magus/ThesisUESTC) 项目修改。

[原项目的 README](https://github.com/x-magus/ThesisUESTC/blob/master/README.md)

[预览 pdf](https://github.com/lyh543/UESTC_LaTeX_Template/blob/master/Course_Thesis/main.pdf)

## 简易的使用手册

### 文件说明

* main.tex: 论文模板
* reference.bib: 论文的参考文件
* pic 文件夹: 论文引用的图片
* main.pdf: 生成的 PDF

### 编译选项

第一次使用 `xelatex -> bibtex -> xelatex -> xelatex` 四次编译。之后如没有修改文献，使用 `xelatex` 编译一次即可。

也可以使用 latex

在 Windows 10 (64 位)，TeXLive 2019 通过编译。

### 其他说明

由于结课论文封面种类繁多，模板只包含摘要后的部分，封面需生成 pdf 后用软件（如 Adobe Acrobat PDF）合并在一起。

## 修改

1. 由于是将学士学业论文修改为结课论文，故将模板中 `thesis-uestc.cls` 的

```
\DeclareOption{bachelor}{
  \def\chinesedegreename{本科}
  \def\englishdegreename{Bachelor}
  \def\chinesebooktitle{文化与思维~结课论文}
  \def\englishbooktitle{Bachelor Thesis}
  \def\display@englishheader{Bachelor Thesis of University of
    Electronic Science and Technology of China}
}
```

等部分删去。

2. 由于结课论文封面种类繁多，故将封面删去，打印好 pdf 后，再使用 pdf 工具（如 Adobe Acrobat Pro）进行拼接。
3. 将 `main.tex` 中结课论文不需要的部分（英文摘要、致谢、攻读学位期间取得的成果、外文资料原文译文）注释。
4. 将多文件版本的 `main_multifile.tex` 和 `misc` 文件夹删去。
5. 由于使用单面打印，将检查单双页的代码注释。