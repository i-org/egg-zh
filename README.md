# 鹅哥哥 成果管理 （Egg = Emacs Got Git).

易码肆常用的版本管理工具，功能较全，交互界面友好，主要操作流程有提示操作，
绝大部分操作有直观的提示，这样可以不用去记复杂的命令，直观使用git的绝大部分功能。
对新手来手比较方便，容易上手。

个人把操作提示都翻译成中文，且调整了有些布局不合理的菜单。

注：此中文名纯属搞笑！
![鹅哥哥](/doc/egg.jpg)

正规的标志是这个
![正规标志](/doc/egg_logo.svg)

## Intro

Egg is an Emacs interface to git. It's a suite composed of a
minor-mode and various special-buffers presenting different UIs to
help the user performing many git operations.

- egg-minor-mode: providing git-specific vc-look-alike interface
  including similar key-bindings, a minor-mode menu and history
  annotations (blame).
- egg's status-buffer:
  - index manipulation/commit preparation
  - interactive rebase stepping
  - merge conflict resolution
  - stashing work-in-progress
  - adding ignore pattern
  - staging new files
  - ediff or ediff3 launching. (e.g. 3-way ediff of
    work-dir/INDEX/HEAD, 3-way ediff of work-dir/theirs/ours)
- egg's log-buffer
  - browse repo's history and reflogs
  - ref (tag, branch, etc) creation and deletion
  - push and fetch
  - start merge/rebase/interactive-rebase session
  - anchor HEAD (reset)
  - search history (pickaxe), grep commit message.
  - compare revisions
- egg's file-log-buffer: restricted version of the log-buffer, used to
  browse history of a single file.
- egg's query:commit-buffer: restricted variation of the log-buffer,
  used to browse history-search's results (pickaxe or message grep)
- egg-grep: a compile-mode which can grep files in non-checkout git
  revisions.
- egg's commit-log-edit buffer: used to compose the commit-message for
  the upcoming commit. it can do some minor index manipulation. gpg-signature
  can also be enabled.
- egg's tag:msg-buffer: used to compose the message of an annotated tag.
  gpg-signature can also be enabled.
- egg's diff-buffer: used to view the delta between file or repo revisions.

 

## Thanks to MAGIT

The design of the status-buffer Egg was borrowed/stolen from Magit.
however has much more functionalities than the status buffer.
Magit is an interface to the version control system Git, implemented
by Marius Voller. His code at: http://philjackson.github.com/magit/
