# iTem2
	* 下載 - [https://www.iterm2.com/](https://www.iterm2.com/)
	* 把它移到應用程式資料夾，並開啟

## 安裝 Homebrew
	* 打開 `iTerm2`
	* 執行指令 `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
	* 顯示版本，執行指令 `brew --version`
	* 檢查，執行指令 `brew doctor`
	* 更新，執行指令 `brew update`
	* 重開 iTerm

## 安裝 Zsh
	* 打開 `iTerm2`
	* 執行指令 `brew install zsh`
	* 執行指令 `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`
	* 重開 iTerm

## 顯示隱藏檔案
	* 打開 `iTerm2`
	* 執行指令 `defaults write com.apple.finder AppleShowAllFiles TRUE;\killall Finder`

## 建立 SSH
	* 打開 `iTerm2`
	* 執行指令 `ssh-keygen -t rsa -C "your_email@example.com"`，your_email@example.com 請改成你的 mail，過程中會要求輸入相關東西，可以直接 Enter 使用預設值跳過
	* 複製公鑰，執行指令 `pbcopy < ~/.ssh/id_rsa.pub`
		* 貼到 [GitHub](https://github.com/)
		* 貼到 [BitBucket](https://bitbucket.org/)
		* 自動登入 Server 的話，貼到 Server 上的 `~/.ssh/authorized_keys`

## 常用設定
	* 啟動 iTerm2 的初始位置
		* 打開 `iTerm2`
		* 快捷鍵 `command + ,`
		* 點選 `Profiles` > `General` > `Working Directory` > 選擇 `Directory`，輸入位置 `/Users/oa/www`
	
	* 修改字型
		* 打開 `iTerm2`
		* 快捷鍵 `command + ,`
		* 點選 `Profiles` > `Text` > `Font` > `Change Font` > 點選 `All Fonts` > 點選 `Hank` > `標準體` > `18`
		* 勾選 `Use a different font for non-ASCII text`
		* 修改 `Non-ASCII Font` > `Change Font` > 點選 `All Fonts` > 點選 `Hank` > `標準體` > `18`
	
	* 調整視窗
		* 打開 `iTerm2`
		* 快捷鍵 `command + ,`
		* 點選 `Profiles` > `Window` > `Settings for New Windows`
		* Columns 調整為 `120`
		* Rows 調整為 `38`
	
	* 調整快捷鍵
		* 打開 `iTerm2`
		* 快捷鍵 `command + ,`
		* 點選 `Keys` > `+`
			* 游標移至最前，快捷鍵為 `command + ←`，Action 選 `Send Hex Code`，輸入 `0x01`
			* 游標移至最後，快捷鍵為 `command + →`，Action 選 `Send Hex Code`，輸入 `0x05`
			* 切換左邊頁籤，快捷鍵為 `command ＋ Shift + ←`，Action 選 `Move Tab Left`
			* 切換右邊頁籤，快捷鍵為 `command ＋ Shift + →`，Action 選 `Move Tab Right`
			* 切換左方分頁，快捷鍵為 `command ＋ control + ←`，Action 選 `Select Split Page on Left`
			* 切換右方分頁，快捷鍵為 `command ＋ control + →`，Action 選 `Select Split Page on Right`
			* 切換上方分頁，快捷鍵為 `command ＋ control + ↑`，Action 選 `Select Split Page on Above`
			* 切換下方分頁，快捷鍵為 `command ＋ control + ↑`，Action 選 `Select Split Page on Below`

