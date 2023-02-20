---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

![bg left:43%](https://catonmat.net/images/why-vim-uses-hjkl/hjkl-tshirt.png)

# **Vim, serious?**

~~How to exit the Vim editor?~~
Text Code Editor

<!-- sed -e '/localhost/r file2' -e "s///" file1 -->

<!--
https://marp.app/
marp cli / marp vs
npx @marp-team/marp-cli@latest slide-deck.md
-->

----

![bg left:30%](https://avatars.githubusercontent.com/u/346761?v=4)

- Shawn Wang 王榮祥
- 成大電通所

<br />

- EasyStack Distro (openstack on k8s)
- Canonical OEM / infra
- 廣達 NB BIOS enginneer

- KaLUG - Kaohsiung Linux User Group [![Telegram](https://img.shields.io/badge/-telegram-red?color=white&logo=telegram&logoColor=blue)](https://t.me/+QX0S5Q0Wg-1r637K)
- [slide:github/shawn111 - editor/editor.md](https://github.dev/shawn111/labs)
- [labs:killercoda](https://killercoda.com/shawn111/)


----

# integrated development environment

https://en.wikipedia.org/wiki/Integrated_development_environment

- Editor
- Code completion, search - [LSP](https://langserver.org/)
- Debug Adapter Protocol - [DAP](https://microsoft.github.io/debug-adapter-protocol/)
- Syntax highlighting - [tree-sitter](https://tree-sitter.github.io/tree-sitter/)
- Version control - git
- lang package manager - [npm](https://www.npmjs.com/) / [cargo](https://crates.io/) / go
- ~~Visual programming (*)~~

----

![bg right:45%](github_repo.png)

- CI/CD
  - testing
    - unit test
    - integration test
  - release
    - package
    - container / Kubernetes
- dev flow
  - github flow
  - pair programming

----

# code editor

- text editor (console)
  - nano / vi / emacs(*) / helix
- gui editor
  - vscode / emacs
- web
  - eclipse theia - ex: [killercoda](https://killercoda.com/examples/scenario/foreground-background-scripts-multi-step-ide)
  - [github.dev](https://github.dev)
  - [vscode.dev](https://vscode.dev)

<!-- HTML comment recognizes as a presenter note per pages. -->
<!-- You may place multiple comments in a single page. -->

----

# why text editor

- console
- lightweight
- remote edit (*)
- not just for coding
  - good for config
  - UNIX - everything is a file

![bg left:43%](https://catonmat.net/images/why-vim-uses-hjkl/lsi-adm-3a.jpg)

----


# vi family
- a screen-oriented text editor
- [Vim Cheat Sheet](https://vim.rtorr.com/)

- [vim](https://github.com/vim/vim) (Vi iMproved) / gvim - c
  - vim7 2006
  - vim8 2016 - after neovim
  - vim9 - [vim9script](https://www.zhihu.com/question/364528657)
- Others: [Neovim](https://github.com/neovim/neovim) - c + lua / Kakoune / helix - rist
  - Embed Neovim everywhere
  - built-in LSP

![bg right](https://github.com/glacambre/firenvim/raw/master/firenvim.gif)

----

# vi modes:

___modes.md___

----

## range / num / sort

___num.md___

----

## Searching And Replacing

___search.md___

----

## Copying And Pasting

___copy.md___

----

## Saving And Quitting

___save.md___

----

### [windows & tabs](https://dev.to/iggredible/using-buffers-windows-and-tabs-efficiently-in-vim-56jc)

___win.md___

----

## key binding

___key.md___

----

# vim plugins

___pligins.md___


----

<!-- ![bg right:53%](https://catonmat.net/images/why-emacs-uses-meta/emacs-lisp-machine-space-cadet-keyboard-full.jpg) -->

# emacs - "Editor MACroS"
- emacs (vi mode- spaceemacs)
- editor war (vi/emacs)
  - simple vs complex
  - mode vs key binding
- LISP
 
![](https://catonmat.net/images/why-emacs-uses-meta/hyper-super-meta-ctrl.jpg)

----

# helix

- Multiple selections
- Tree-sitter integration
- Powerful code manipulation
  - Navigate and select functions, classes, comments, etc and select syntax tree nodes instead of plain text. 
- Language server support
- Modern builtin features
  - config-less
- Debug Adapter Protocol (WIP)

----

# Tree-sitter


```
            ┌────┐                     - Lang binding
            │call│                     - parsers
      ┌─────┴────┴─────┐
      │                │
┌─────▼────┐      ┌────▼────┐
│identifier│      │arguments│
│  "func"  │ ┌────┴───┬─────┴───┐
└──────────┘ │        │         │
             │        │         │
   ┌─────────▼┐  ┌────▼─────┐  ┌▼─────────┐
   │identifier│  │identifier│  │identifier│
   │  "arg1"  │  │  "arg2"  │  │  "arg3"  │
   └──────────┘  └──────────┘  └──────────┘
```


----

# LSP

![](https://microsoft.github.io/language-server-protocol/img/vscode-css-code-complete.png)

----

## select and action

===select.md===

----

## Tree-sitter Textobject Based Navigation

===code-move.md===

----

## support status

===health.md===



----

## space mode (helix)

===space.md===

----

## ctags

- generates an index (or tag) file of language objects found in source files

- [Vim 8 中 C/C++ 符号索引：GTags 篇](https://zhuanlan.zhihu.com/p/36279445)
- universal-ctags


----

# C/C++ LSP server

- [clangd](https://clangd.llvm.org/): part of the llvm project
- [ccls](https://github.com/MaskRay/ccls): more features

https://emacs-china.org/t/topic/6428
