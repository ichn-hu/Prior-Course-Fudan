# 贡献本网站

本课程主页是用 mkdocs 生成并托管在 GitHub 上的静态网站，使用了 utterance 作为评论系统。

## 环境搭建

mkdocs 是用 python 编写的文档生成器。为了使用 `mkdocs` 构建本站，你需要配置好 python 环境，并安装 `mkdocs`。

推荐使用 `anaconda` 来管理环境。

!!! note "python 环境配置"
    请看这个[页面](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)。
    TODO: 添加 python 安装的教程，包括配置清华源

在配置好 python 环境后，你就可以安装 `mkdocs` 和对应的主题了，

```bash
conda create -n mkdocs
conda activate mkdocs
conda install pip
# 上述三步是可选的，用 anaconda 新建一个名为 mkdocs 的环境，并激活它，然后为其安装 pip （ python 的包管理器）
pip install mkdocs
pip install mkdocs-material
```

这两步完成后（对的，实际上就只有两步，安装 `mkdocs` 和 `mkdocs-material` 就行了），你就可以构建本网站了。

如果遇到任何问题或者想知道更多，可以参考 mkdocs 的[文档](https://www.mkdocs.org/#installation)。

## 构建本站并在本地预览

首先你需要把网站的源代码从 GitHub 上扒到你的电脑上。本网站的所有内容都开源在 GitHub 上：[https://github.com/ichn-hu/Prior-Course-Fudan](https://github.com/ichn-hu/Prior-Course-Fudan)

```bash
git clone https://github.com/ichn-hu/Prior-Course-Fudan.git
```

## mkdocs 主题

我们使用 [mkdocs-material](https://squidfunk.github.io/mkdocs-material/) 作为网站的主题。关于该主题的配置与使用，请参考[链接](https://squidfunk.github.io/mkdocs-material/)

## 文件结构

mkdocs 的配置文件为 `/mkdocs.yaml`, 本网站使用非默认的配置，所有的内容文档存放在 `/content/` 文件夹下，内容文档使用 [`markdown` 语法]()进行编写。

## 注册 github 帐号

Github 是一个托管由 git 管理的项目的地方。

众所周知程序开发过程中会经历很多次的版本迭代和代码改动，因此我们需要一个工具来帮忙记录程序变动，git 便是一个这样的软件版本控制软件（fun facts: git 和 Linux 操作系统共享一个爸爸——Linus）。

而 GitHub 便是目前最大的项目托管平台，是代码开源运动的主力战场。很多程序员都愿意把自己的项目开源在 github 上以吸♂引其他程序员的围观和合作。

本站也不例外，虽然主要是以内容为主的静态站点，但内容都通过 MIT License 开源在 github 上。

## 提交 Pull Request 帮助修改文章

如果你发现网站上的文章存在

* 错别字（ typo ）
* 描述不清楚
* 内容不完善
* 等其他你认为可以被改善的地方

你可以点击页面右上角的「铅笔」符号从而编辑修改文章内容。注意本站点的文章都是使用 markdown 语法书写，在改动之前你可能需要[学习一下 markdown 写作规范](https://juejin.im/post/5c21ea45e51d453634701bca)。

### 在 github 上协作的基本流程

一般而言你需要先 fork 本代码仓库到你的帐号下，因为出于安全考虑只有仓库拥有者才能直接修改仓库内容（谨防删库跑路）。当你点击上面的修改符号的时候，github 会为你自动 fork 本代码仓库。

然后你可以尽情地在你自己 fork 的代码仓库下做修改，修改之后通过名为 `commit` 的操作把你的修改提交到 git 历史中去。这时，你 fork 的代码仓库的历史会比我们管理的代码仓库的历史更新，这个时候你就可以发起一次 pull request。

所谓 pull request 就是请求将你的改动合并到我们管理的代码仓库中去，随后我们会帮你 review 你的改动，如果我们认为你的改动有效我们就会同意你的请求，将你的 pull request 合并到主代码仓库中来，随后自动构建和自动部署会被触发，你的改动就会被呈现在网站上！

这样你就完成了一次有分量的贡献，感谢！

### 使用 git 在本地进行修改

## 提交建议

如果你对网站的内容、结构、形式等任何地方有建议，可以在本站的 [issue 区](https://github.com/fudan-today/tech/issues)提交一个 issue 。如果你有能力去实现这个建议，我们会更加欢迎你的贡献的！