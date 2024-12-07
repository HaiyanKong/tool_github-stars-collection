---
project: typora-latex-theme
stars: 4920
description: 将Typora伪装成LaTeX的中文样式主题，本科生轻量级课程论文撰写的好帮手。This is a theme disguising Typora into Chinese LaTeX style.
url: https://github.com/Keldos-Li/typora-latex-theme
---

Typora 伪装 LaTeX 中文样式主题
======================

下载与安装 | 帮助文档 | 个性化设置 | 贡献指南 | 技术细节 | 常见问题

本项目的初衷是为了简化中国大陆本科生**小型通识课论文**（或**小型实验报告**）撰写的负担。这里基本采用了浙江大学要求的格式（字体较小，页边距较小），但大部分同学都可以自行在 CSS 中修改适合自己学校的格式。

Markdown 的轻量化特性，使您可以专注于论文内容而不用担心格式。书写时仅通过简单的标记，并通过替换样例模板中的个人信息，您就可以输出类 LaTeX 排版的精美论文与报告。本项目支持 Windows, macOS 和 Linux 三大平台的 Typora。

预览
--

您可以通过以下方式预览本主题：

1.  通过在线 PDF 预览器预览导出结果
2.  观看介绍视频，其中简洁清晰地介绍了主题外观和安装方法
3.  查看下列截图

### 封面，摘要和关键词

### 预览与编写

#### 层级标题

#### 表格

表格：

<center\><strong\>表 2  全球/中国桌面操作系统市场份额占比（%）</strong\></center\>

| OS   | Windows | macOS | Unknown | Linux | Chrome OS | 其他 |
| ---- | ------- | ----- | ------- | ----- | --------- | ---- |
| 全球 | 76.56   | 17.1  | 2.68    | 1.93  | 1.72      | 0.01 |
| 中国 | 87.55   | 5.44  | 6.24    | 0.75  | 0.01      | 0.01 |

#### 项目列表

#### 代码块

#### Mermaid

mermaid 图形：

​\`\`\`mermaid
graph LR
A(开始) -->
input\[/输入a,b/\] --> if{a%b=0 ?}
if --->|yes| f1\[GCD = b\] --> B(结束)
if --->|no| f2\["a, b = b, a % b "\]\-->if
​\`\`\`

#### 公式

公式：

$$
\\iint\\limits\_{x^2 + y^2 \\leq R^2} f(x,y)\\,\\mathrm{d}x\\,\\mathrm{d}y = \\int\_{\\theta\=0}^{2\\pi} \\mathrm{d}\\theta\\int\_{r=0}^R f(r\\cos\\theta,r\\sin\\theta) r\\,\\mathrm{d}r\\, \\tag{1}
$$

下载与安装
-----

**请完整阅读以下过程，以确保一切符合预期。**

1.  Typora 是一个支持实时预览的 markdown 编辑器。在安装本主题前，请确认您已下载 Typora 并完成了安装。如果您对 markdown 的语法还不了解，您可以从这里获得帮助。
    
2.  前往本项目的 release 页面，下载适合您操作系统的最新版本压缩包。比如，如果您在使用 Windows 操作系统，您就应该下载 `latex-theme-windows.zip`。
    
3.  解压缩这个文件，进入解压缩后的文件夹。按照在线安装教程或该文件夹下 `README.md` 中的安装教程**完成剩余的安装步骤**。请务必确认您完成了下面的步骤：
    
    -   进行手动或自动主题安装
    -   下载并安装所需的字体

鸣谢
--

本项目是在下面两个开源项目的基础上完成的：

-   yfzhao20/Typora-markdown
-   du33169/typora-theme-essay\_cn

感谢 @大啊好我r中之 制作介绍视频
