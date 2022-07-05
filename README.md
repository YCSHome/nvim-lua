# 用lua配置你的nvim

此文章同步更新于 [github](https://github.com/YCSHome/nvim-lua) 上

## 前言：

### 关于 neovim

`neovim` 是一个 very great 的 `vim` 船型升级版。不过相对于更新较为缓慢的 `vim` ~~(这货今年七月才出 `vim9.0`)~~，`neovim` 的更新更加激进且快速。最典型的例子就是在 `neovim 7.0` 中彻底放弃了对 `python 2.x` 的支持。

不过与之带来的就是与新时代更好的兼容与便捷，比如可以采用 `lua` 这样极为快速的脚本语言进行配置，`vim9.0` 速度也只能勉强赶上，更不用提之前的 `vimscript` 了。同时 `neovim` 内置了一些列有趣的东西，比如浮动终端、tree-sitter和Virtual Text。

![](../photo/virutal_text_example1.png)

![](https://cdn.luogu.com.cn/upload/usericon/311721.png)

为什么们需要 `lua` 这个奇妙的语言？

因为它快（起码是我已知的脚本语言里面排前三的）

而且 `vim9.0` 已经发布了，可爱的 vim 党们多少都要重新学语言了，（顺便学个lua也没什么大不了）
