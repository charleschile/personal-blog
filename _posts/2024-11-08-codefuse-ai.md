---
layout: distill # post or distill
title: Contributions to CodeFuse-AI
date: 2024-11-06
description: this is a record of my contributions to the CodeFuse, especially the modelcache
tags: open-source, LLM, cache
categories: open-source
tabs: true
featured: true
toc: true


# giscus_comments: true


# authors:
#   - name: Albert Einstein
#     url: "https://en.wikipedia.org/wiki/Albert_Einstein"
#     affiliations:
#       name: IAS, Princeton

# toc:
#   - name: 1.1 Equations
#     # if a section has subsections, you can add them as follows:
#     subsections:
#       - name: Example Child Subsection 1
#       - name: Example Child Subsection 2
#   - name: First tabs
#     subsections:
#       - name: Example Child Subsection 3
#       - name: Example Child Subsection 4
#   - name: Footnotes
#   - name: Code Blocks
#   - name: Interactive Plots
#   - name: Layouts
#   - name: Other Typography?

toc:
  - name: Development Pitfalls
    subsections:
      - name: 1. numpy与python版本不兼容兼容


---



## Tech Knowledge

### 1. Docker

docker在概念上与虚拟机十分类似，但却轻量很多

镜像Image，一个虚拟机的快照snapshot，里面包含了你要部署的应用程序以及他所关联的所有的库，通过镜像我们可以创造很多的容器

容器 container，容器是各自独立的虚拟机

Dockerfile: 是脚本，主要用来创建镜像



RUN是创建镜像的时候使用的命令

CMD是创建容器的时候使用的









## Development Pitfalls

### 1. numpy与python版本不兼容兼容

[NumPy 1.24.4 Release Notes](https://numpy.org/devdocs/release/1.24.4-notes.html): The Python versions supported by this release are 3.8-3.11.

所以需要先将我的python版本从3.12降到3.11

#### 使用 pyenv 安装和管理 Python 版本
pyenv 是一个用于管理多版本 Python 的工具，推荐用于开发环境。

安装 pyenv： 如果你还没有安装 pyenv，可以使用 Homebrew 安装：

```
brew install pyenv
```

安装 Python 3.11：
```
pyenv install 3.11.6  # 选择你想安装的具体版本

```

设置全局 Python 版本：

```
pyenv global 3.11.6
```
在当前 shell 环境中启用 pyenv：

```
echo 'eval "$(pyenv init --path)"' >> ~/.zshrc
source ~/.zshrc

```