## 設定 Git 版本控制軟體

  * 用 Sublime Text 2 打開編輯 `~/.gitconfig`，終端機執行指令 `subl ~/.gitconfig`
  * 將內容修改成如下，主要針對 `user` 與 `alias` 做修改

```
[user]
  name = OA Wu
  email = comdan66@gmail.com

[alias]
  st = status
  co = checkout
  rb = rebase
  cp = cherry-pick
  ci = commit
  ss = stash
  cn = clean
  pu = push origin
  ps = push origin
  sl = shortlog -s -n
```

## 修改 git 編輯器改用 Sublime Text 2
  * 終端機執行指令 `git config --global core.editor "subl -n -w"`
