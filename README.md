# MarkSearch

## Husky-本地hook

pre-commit

post-commit

pre-push

## Github Action-远程hook

post-push

## Test

11

## 开发-构建-发布

build_version: 1.0.0

commit 主要用于保存代码,一般不会触发自动构建,每次commit自动递增第3位

push 主要用于构建,一般会触发自动化构建+自动化测试+自动化部署,每次commit自动递增第2位,重置后面的位

- 用origin的最近一次成功的构建来兜底,方便来本地各种折腾时可以随时用远程来回退.因为本地经常把commit当做Ctrl+S来用了,有时候经常会找不到上一次成功的运行是哪一个commit了.这时候,查看git tag 有origin/main 这个tag的就是最近的成功构建了.

release 主要用于发布.一般会先经过MR的代码评审,再合并到main分支,每次commit自动递增第1位,重置后面的位


## 将源码和产物拆分仓库

[源码仓库: fishyer/marksearch-obsidian](https://github.com/fishyer/marksearch-obsidian)
[产物仓库: fishyer/MarkSearch-Obsidian-dist](https://github.com/fishyer/MarkSearch-Obsidian-dist)
