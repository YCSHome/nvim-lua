# 用lua配置你的nvim

~~in fact，到现在我都没写完~~

此博客同步更新于 [github](https://github.com/YCSHome/nvim-lua) 上

## 前言：

### 关于 neovim

`neovim` 是一个 very great 的 `vim` 船型升级版。不过相对于更新较为缓慢的 `vim` ~~(这货今年七月才出 `vim9.0`)~~，`neovim` 的更新更加激进且快速。最典型的例子就是在 `neovim 7.0` 中彻底放弃了对 `python 2.x` 的支持。

不过与之带来的就是与新时代更好的兼容与便捷，比如可以采用 `lua` 这样极为快速的脚本语言进行配置，`vim9.0` 速度也只能勉强赶上，更不用提之前的 `vimscript` 了。同时 `neovim` 内置了一些列有趣的东西，比如浮动终端、tree-sitter和Virtual Text。

为什么们需要 `lua` 这个奇妙的语言？ 因为它快（起码是我已知的脚本语言里面排前三的）

而且 `vim9.0` 已经发布了，可爱的 vim 党们多少都要重新学语言了，（顺便学个lua也没什么大不了）

### 关于本博客

这个博客目前的定位是面向有一定 vim、neovim 使用经验的人，至于 0 基础的小白会之后考虑加入相关的内容。不过 0 基础的小白不建议直接上手 neovim。

这篇博客会结合我自身的使用经验和官方文档进行讲述，尽可能保证自己讲述清楚。同时会列举相当多的插件，所以可能最后的效果只适合自己日常使用而不能应用于线下赛。（毕竟现在的比赛电脑连 neovim 都没有）
所以这篇博客更加注重于配置文件的编写与插件配置，而不会在基础上纠结太久。

不过我本人没有用过 MacOS，所以面对 MacOS 部分我可能无法讲得很详细很准确，还请多多包涵。

## 目录：

- 开始？
  - 从下载开始
  - 自己的第一个 neovim 配置文件

## 开始

### 从下载开始

[github](https://github.com/neovim/neovim/releases/latest) 上的发布页面，或者是 [官网](https://www.neovim.io)，（虽然说这个官网最后也是跳到 github 上的 wiki 去）

### 自己的第一个 neovim 配置文件

什么？这么快就跑到配置文件去了？？！！

没错，这篇博客已经将你定位为一名有部分经验的 vimer 而不是单纯的锰锌。

Windows 下，neovim 的配置文件位于 `$USERRPROFILE$\AppData\Local\nvim\init.vim` 中，

Linux 或者说是 MacOS 中，（官方文档说是 Unix 系统……）配置文件位于 `~/.config/nvim/init.vim`，

一般 neovim 是没有全局配置文件的（好吧也可能是我不知道），所以每一个用户的配置文件都是独立的。

对于我们的 init.vim，我们可以用对待 vim 的方式对待它。

``` vim
set nu
syntax enable
syntax disable
```
