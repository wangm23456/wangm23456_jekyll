---
layout: post
title: linux生存指南#1
category: linux
---

<p class="message">
    关于一些软件的配置和错误解决记录
</p>

# 1. sublime text 3

## Bug

1.  中文输入法修复：[sublime-text-imfix](https://github.com/lyfeyaj/sublime-text-imfix)
2.  解决中文下沉：首选项->设置：添加以下代码

    ~~~ json
     {
        "font_face" : "SourceHanSansSC"
    }
    ~~~

4.  OmniMarkupPreviewer问题：

    >Error: 404 Not Found
    >Sorry, the requested URL 'http://127.0.0.1:51004/view/31' caused an error:
    >buffer_id(31) is not valid (closed or unsupported file format)'
    >**NOTE:** If you run multiple instances of Sublime Text, you may want to adjust
    >the `server_port` option in order to get this plugin work again.

     [方法](http://stackoverflow.com/questions/35798823/omnimarkuppreviewer-404)
     Sublime Text > Preferences > Package Settings > OmniMarkupPreviewer > Settings - User

    加入以下代码：

    ~~~ json
      {
      "renderer_options-MarkdownRenderer": {
         "extensions": ["tables", "fenced_code", "codehilite"]
           }
       }
    ~~~

## Package
1. Package control：[package control installation](https://packagecontrol.io/installation)
2. 主题：material-theme:

    ![material](http://ww2.sinaimg.cn/mw690/66c92bc3gw1f8ngt4qtzaj218g0o9n6j.jpg)

3. MarkdownEditing
4. MarkdownTOC
5. omnimarkuppreviewer
6. TableEditor
7. Emmet:[前端开发必备！Emmet使用手册](http://www.w3cplus.com/tools/emmet-cheat-sheet.html)
8. etc.

# 2. Zsh & Oh My Zsh
[Zsh](http://www.zsh.org/) Zsh 是一款功能强大终端（shell）软件，既可以作为一个交互式终端，也可以作为一个脚本解释器。它在兼容 Bash 的同时 (默认不兼容，除非设置成 emulate sh) 还提供了很多改进，例如：
* 更高效
* 更好的自动补全
* 更好的文件名展开（通配符展开）
* 更好的数组处理
* 可定制性高

[Oh My Zsh](http://ohmyz.sh/) 是Zsh的配置工具，包括很多主题、插件。

# 3. 桌面

## 字体&Gnome theme

[INPUT](http://input.fontbureau.com/)，把ttf文件放在~/.fonts下即可。

[Pather-OSX](https://www.gnome-look.org/p/1150507/)，放在/usr/share/themes下

[Oranchelo icons](https://www.gnome-look.org/p/1151321/)

[Capitaine Cursors](https://www.gnome-look.org/p/1148692/)

## Docky

一个启动器。

# 4. Terminator
1. 安装：[office](http://gnometerminator.blogspot.jp/p/introduction.html)

    >sudo add-apt-repository ppa:gnome-terminator
    >sudo apt-get update
    >sudo apt-get install terminator

2. 配色方案：在 ~/.config/terminator/config 中添加配置代码：[iTerm2](https://github.com/mbadolato/iTerm2-Color-Schemes)

# 5. Guke Terminal
[Guake](http://guake-project.org/)是一个下拉式终端，默认`<F12>`呼出。

# 6. 星际译王
1. 安装: [StarDict](http://stardict-4.sourceforge.net/index_cn.php)
2. 离线词典：[各种词典](http://abloz.com/huzheng/stardict-dic/zh_CN/)

# 7. 迅雷
作者已弃坑：[Xware Desktop](https://github.com/Xinkai/XwareDesktop)

# 8. 键鼠共享
1. [代码](https://github.com/symless/synergy)
2. [nightly版](https://symless.com/nightly)

# 9. Dukto
传输工具，搭配synergy食用，局域网互传文件利器。

[介绍](http://www.iplaysoft.com/dukto.html)

[官网](http://www.msec.it/blog/?page_id=556)

# 10. GDebi
软件编译安装工具。

# 11. QtiPlot
linux上的origin,[QtiPlot](http://www.qtiplot.com/)

# 12. learnote
[learnote](https://leanote.com/)

一款跨平台的笔记应用，支持markdown。

# 13. Game

## Dwarf Fortress
大名鼎鼎的**矮人要塞**，上手难度恐怖。

[wiki:lazy newb package](http://dwarffortresswiki.org/Utility:Lazy_Newb_Pack)

[Unofficial Linux Lazy Newb Pack](http://www.bay12forums.com/smf/index.php?PHPSESSID=86ecf689a693ec3100c23e04c2f89d4f&topic=156011.msg6784657#msg6784657)

## Tales Of Maj'Eyal: Age Of Ascendancy
[马基埃亚尔的传说](https://te4.org/)，Rogulike-RPG，最优秀的Roguelike游戏之一。

