# 北京大学信息科学技术学院 2025 年本科生毕业论文 LaTeX 模板

## 用法

1. 确保你的电脑是 Windows 系统，安装了 TeX Live 2025。
   - 为啥是 TeX Live？
     - MiKTeX 确实没测试过，但我猜测是可以的，毕竟我以前是 MiKTeX 用户。
     - 其实我用的是 TinyTeX，一个精简的 TeX Live。但是得手动安装宏包。
   - 为啥是 Windows？
     - 我调用了 Windows 自带的楷体和中易仿宋。
     - 我认为 Linux 用户有能力解决问题。
     - 我买不起 mac。
2. 去右边的 Release 下载最新版本。
3. 解压缩，安装 fonts 里的字体。具体而言：
   - 对于 Windows 10，选择所有字体，右键，“为所有用户安装”
   - 对于 Windows 11，选择所有字体，右键，“显示更多选项” -> “为所有用户安装”
   - 字体装了一次就不用再装了，换句话说，更新模板的时候，下载 `Source code.zip`，提取其中的 `pkuthesis.cls` 就行。
4. 在 `example.tex` 写论文。

   我知道用一堆 `\newcommand` 定义标题导师什么的很恶心，但我懒得搞更高级的实现了。

   标题的字号可调，例如：

   ```latex
   \newcommand{\preTitleCn}{\zihao{2}}
   \newcommand{\preTitleEn}{\zihao{3}}
   ```
5. 使用 LuaLaTeX 编译。如果你有参考文献，可能还需要 biber。

   这玩意编译很慢，首先 LuaTeX 就慢，其次我调了一堆字体会更慢，最后用 `tabularray` 画表格慢死了（是的没错，封面是表格画的）。

## 免责声明

1. 本模板并非北京大学官方制作。
2. 本模板处于极早期开发阶段，功能不全，仅包含封面、目录、正文、参考文献。
3. 本模板可能出现各种格式错误，由此造成的后果我概不负责。
4. 你可以以任何方式使用本模板的代码部分，包括二次修改/销售，但出现问题别来找我。
5. 模板使用的北京大学标志与中文校名组合（`PKU-Logo.pdf`）来自[北京大学标识管理办公室](https://vim.pku.edu.cn/)。
6. 本模板使用的字体遵循各自的开源许可，它们是：
   - Inter
   - JetBrains Mono
   - Nimbus Roman No.9 L
   - 思源宋体
   - 思源黑体

   此外，本模板调用了 Windows 系统中的楷体和中易仿宋。
