# 安裝 iTem2 終端機

  * 官網下載 - [https://www.iterm2.com/](https://www.iterm2.com/)
  * 備用載點 - [iTerm2-3_2_0.zip](https://cdn.ioa.tw/MacEnvInit/iTerm2-3_2_0.zip)
  * 解壓縮，把它移到**應用程式資料夾**，並開啟

## 安裝 Homebrew

  * 終端機執行指令 `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
  * 顯示版本，終端機執行指令 `brew --version`
  * 檢查，終端機執行指令 `brew doctor`
  * 更新，終端機執行指令 `brew update`
  * 重開 iTerm

## 安裝 Zsh

  * 終端機執行指令 `brew install zsh`
  * 終端機執行指令 `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
  * 重開 iTerm

## 建立 SSH

  * 終端機執行指令 `ssh-keygen -t rsa -C "your_email@example.com"`，your_email@example.com 請改成你的 mail，過程中會要求輸入相關東西，可以直接 Enter 使用預設值跳過
  * 複製公鑰，終端機執行指令 `pbcopy < ~/.ssh/id_rsa.pub`
    * 貼到 [GitHub](https://github.com/)
      * 右上頭像 > `Setting` > `SSH and GPG keys` > `New SSH Key`，貼上公鑰
    * 貼到 [BitBucket](https://bitbucket.org/)
      * 左下頭像 > `View profile` > `Settings` > `SSH keys` > `Add Key`，貼上公鑰
    * 自動登入 Server 的話，貼到 Server 上的 `~/.ssh/authorized_keys`

## 常用設定
快捷鍵 `command + ,` 開啟設定

  * `Profiles`，先選擇左邊的 `Default` 再進行以下設定
    * `General` > `Working Directory` > `Directory`，輸入位置開啟時的位置 `/Users/oa/www`
    * `Text` 
      * `Font` > `Change Font` > 點選 `All Fonts` > 點選 `Hank` > `標準體` > `18`
      * 勾選 `Use a different font for non-ASCII text`
      * 修改 `Non-ASCII Font` > `Change Font` > 點選 `All Fonts` > 點選 `Hank` > `標準體` > `18`
    
    * `Window` > `Settings for New Windows`，Columns 調整為 `120`，Rows 調整為 `38`
	
	* 調整快捷鍵

  * `Keys`
    * 游標移至最前，此組設定已經存在，快捷鍵為 `command + ←`，Action 選 `Send Hex Code`，輸入 `0x01`
    * 游標移至最後，此組設定已經存在，只要修改 Action，快捷鍵為 `command + →`，Action 選 `Send Hex Code`，輸入 `0x05`
    * 切換左邊頁籤，點選 `+` 新增，快捷鍵為 `command ＋ option + ←`，Action 選 `Next Tab`
    * 切換右邊頁籤，點選 `+` 新增，快捷鍵為 `command ＋ option + →`，Action 選 `Previous Tab`
    * 切換左方分頁，點選 `+` 新增，快捷鍵為 `command ＋ control + ←`，Action 選 `Select Split Page on Left`
    * 切換右方分頁，點選 `+` 新增，快捷鍵為 `command ＋ control + →`，Action 選 `Select Split Page on Right`
    * 切換上方分頁，點選 `+` 新增，快捷鍵為 `command ＋ control + ↑`，Action 選 `Select Split Page on Above`
    * 切換下方分頁，點選 `+` 新增，快捷鍵為 `command ＋ control + ↑`，Action 選 `Select Split Page on Below`

