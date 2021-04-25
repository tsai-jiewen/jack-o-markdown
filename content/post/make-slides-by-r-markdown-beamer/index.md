---
title: Make Slides by R Markdown Beamer
date: 2021-04-25T14:16:37.169Z
draft: false
featured: false
authors:
  - Jiewen Tsai
tags:
  - R
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
## 1 R Markdown

- You just follow the basic R presentation way. do not need any another pkg, but `tinytex`.

![Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled.png](Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled.png)

## 2 YAML settings (the most imp. part)

```yaml
---
title: A minimal example
subtitle: With a subtitle
author: Matthias Vogelgesang
institute: Centre for Modern Beamer Themes
date: \today
header-includes:
  - \usepackage{ctex}
  - \usepackage{xeCJK}
  - \setCJKmainfont{DFKai-SB}
mainfont: Calibri
theme: Madrid
output: 
  beamer_presentation:
    latex_engine: xelatex
fontsize: 12pt
---
```

- use LaTex pkg: `{ctex}` and `{xeCJK}` for Chinese fonts.
- `\setCJKmainfont` can set Chinese font (in the xeCJK or your local computer? )you want, e.g. `{DFKai-SB}` (標楷體)。
- mainfont: you can use CJK fonts or English fonts. Cuz I prefer **Kai+Calibri** setting, so I choose 'Calibri' as the mail font.
- theme: you can visit Beamer theme gallery [here](https://deic-web.uab.cat/~iblanes/beamer_gallery/index.html) to select your favorite theme.
- Output: it is important to apply the `xelatex` engine that your Chinese words can be displayed. On the other hand, if you have another R pkg such as `binb` (binb: Binb is not Beamer)(see the doc [here](https://www.rdocumentation.org/packages/binb/versions/0.0.6)), then the `xelatex` engine will be set default.
- font: Cuz the RBeamer is dependent on LaTex engine, so only 8pt, 9pt, 10pt, 11pt, 12pt, 14pt, 17pt, 20pt are available sizes. The default font size is 11pt, but using Chinese fonts, I suggest 12pt is a better choice.

## 3 Another tips

- `\alert{}` can turn a string's color to red. (Note: black or \textbf{} can not be available in Chinese words)
- Level 3 heading: (### Some enumeration) will be a block. see below:

![Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled%201.png](Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled%201.png)

- Level 2 heading is a new slide title (in beamer, you do not need dash `---` to separate slide. but if you have a too-long paragraph, you can still use `—-`).
- Level 1 heading is a lone, center slide, see below:

![Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled%202.png](Make%20Slides%20by%20R%20Markdown%20Beamer%2051de6620fa7b497b99a55a1ca1742cc6/Untitled%202.png)
