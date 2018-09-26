# 設定 Xcode 與基礎環境

## App Store
  * 重新設定國籍
  
  * 下載安裝 Xcode - [https://itunes.apple.com/tw/app/xcode/id497799835?mt=12](https://itunes.apple.com/tw/app/xcode/id497799835?mt=12)
  * 下載安裝 Line - [https://itunes.apple.com/tw/app/line/id539883307?mt=12](https://itunes.apple.com/tw/app/line/id539883307?mt=12)
  * 下載安裝 LunarCal - [https://itunes.apple.com/tw/app/lunarcal/id459976036?mt=12](https://itunes.apple.com/tw/app/lunarcal/id459976036?mt=12)
    * 基本選項
      * 在登入時自動開啟 `勾選` 
      * 游標停滯時自動滑出 `取消勾選` 
      * 游標離開時自動關閉 `取消勾選` 
      * 地區改為 `台灣`
      * 顯示日期與時間 `取消勾選`
  * 下載安裝 Sip(Apple Store 已無販售)
    * 下拉點選齒輪
      * General
        * Number of colors in color history `取消勾選`
      * Formats
        * CSS 將 All caps `取消勾選`
        * 將不必要的類型 `取消勾選`
      * Shortcuts
        * 只留 `General` 的 `Show Magnifier`，並且設定快捷鍵為 `command + shift + e`

## 建立截圖位置

  * 終端機執行指令 `cd ~/Pictures`
  * 終端機執行指令 `mkdir 截圖`
  * 終端機執行指令 `defaults write com.apple.screencapture location ~/Pictures/截圖`

## 建立 www 資料夾
  
  * 終端機執行指令 `cd ~`
  * 終端機執行指令 `mkdir www`
  * 終端機執行指令 `chmod 777 www`

## Finder 設定
  
  * 上方 `顯示方式`
    * 開啟 `顯示標籤列`
    * 開啟 `顯示狀態列`
    * 開啟 `顯示路徑列`

  * 選用直欄顯示，用快捷鍵 `command + 3`

  * 直欄設定快捷鍵 `command + j`
    * 文字大小 `16`
  
  * `偏好設定`，快捷鍵 `command + ,`
    * 一般
      * 開啟新 Finder 視窗時顯示，改為 `www`
    * 進階
      * 執行搜尋時，改為 `搜尋目前的檔案夾`

  * 左邊側邊欄順序
    * Home
    * AirDrop
    * 應用程式
    * 文件
    * 圖片
    * 下載項目
    * 截圖
    * www
  * 下方 Dock
    * `下載項目` > `右鍵` > `檢視內容方式` > `格狀`


## 系統偏好設定
  * 一般
    * `勾選` 使用暗色選單列和 Dock
    * 側邊欄圖像大小 `大`
    * 最近使用過的項目 `無`
  * Dock
    * 大小拉到約 `五分之一`
    * `勾選` 放大，並且拉到 `最大`
    * `勾選` 自動隱藏顯示 Dock
  * Mission Control
    * 鍵盤和滑鼠快捷鍵全部取消
  * Spolight
    * 全部 `取消勾選`
  * 通知
    * `勿擾模式` 當顯示器進入睡眠時 `勾選`
  * 鍵盤
    * 鍵盤
      * 按鍵重複，`快`
      * 重複前暫延，`短`
    * 快速鍵
      * `Launchapp 與 Dock`
        * 啟用/停用隱藏 Dock `取消勾選`
        * 顯示 Launchapp 設定為 `F4`
      * `螢幕快照` > `拷貝所選區域的圖片至剪貼簿` > 改為 `command + shift + 5`
      * `Spolight` > 全部 `取消勾選`
      * `輔助說明` > 全部 `取消勾選`
      * `App 快速鍵`
        * 按 `+` > 應用程式選 `Finder` > 選單名稱輸入 `顯示上一個標籤頁`，鍵盤快捷鍵設定 `command + option + ←`
        * 按 `+` > 應用程式選 `Finder` > 選單名稱輸入 `顯示下一個標籤頁`，鍵盤快捷鍵設定 `command + option + →`
  * 滑鼠
    * 捲動方向 `取消勾選`
    * 軌跡速度 `第四線`
    * 捲動速度 `第五線`
    * 按兩下的速度 `倒數第三線`
  * 觸碰式軌跡版
    * 點按
      * 除了 `靜音點按` 其他都 `勾選`
      * `按一下` 拉到 `輕微`
      * `軌跡速度` 拉到 `倒數第四線`
    * 捲動與縮放
      * 只勾選 `放大或縮小`
    * 更多手勢
      * 只勾選 `在頁面之間滑動`
  * iCloud
    * iCloud Driver 取消
    * 照片 取消
    * 郵件 取消
    * 聯絡資訊 `勾選`
    * 行事曆 `勾選`
    * 提醒事項 `勾選`
    * Safari 取消
    * 備忘錄 `勾選`
    * Siri 取消
    * 鑰匙圈 `勾選`
    * 返回我的 Mac 取消
    * 尋找我的 Mac `勾選`
  * 藍芽
    * 在選單列中顯示藍芽 `勾選`
  * 共享
    * 修改電腦名稱
  * 日期與時間
    * 時鐘
      * 選擇 `數字`
      * 除了 `使用 24 小時制` 其他都 `勾選`
      * 語音報時 `取消勾選`
  * 輔助說明
    * 滑鼠與觸控式軌跡板
      * `觸控式軌跡板選項` > `啟用拖移` > `三指`

## 顯示隱藏檔案

  * 終端機執行指令 `defaults write com.apple.finder AppleShowAllFiles TRUE;\killall Finder`

## 關閉按住輸入重音字元

  * 終端機執行指令 `defaults write -g ApplePressAndHoldEnabled -bool false`

