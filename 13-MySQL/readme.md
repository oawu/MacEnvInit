# 安裝 MySQL 資料庫

  * 頁面下方 `No thanks, just start my download.` 點擊下載 - [http://dev.mysql.com/downloads/file.php?id=454017](http://dev.mysql.com/downloads/file.php?id=454017)
  * 備用載點 - [mysql-5.6.21-osx10.9-x86_64.dmg](https://cdn.ioa.tw/MacEnvInit/mysql-5.6.21-osx10.9-x86_64.dmg)
  * 對 `mysql-5.6.21-osx10.9-x86_64.dmg` 點擊兩下進行安裝，點擊兩下 `mysql-5.6.21-osx10.8-x86_64.pkg` 開始安裝
  * :exclamation: 若是 OSX 10.10 以上，請在 `安裝類型` 的步驟時點擊 `自訂`，把 `Startup Item` 選項 `取消勾選`！
  * 安裝完成後，打開 `系統偏好設定` > `MySQL` > `Start MySQL Server`
  * 若 `系統偏好設定` 裡面沒看到 `MySQL` 的話，請重開 `系統偏好設定`

## 加入指令
  
  * 用 Sublime Text 2 打開編輯 `~/.zshrc`，終端機執行指令 `subl ~/.zshrc`
  * 在檔案最下面新增 `export PATH="/usr/local/mysql/bin:$PATH"`
  * 重開終端機

## 設定密碼
  
  * 打開 `iTerm2` 終端機
  * 進入 MySQL，終端機執行指令 `mysql -u root`
  * 執行指令 `use mysql;` 選擇資料庫
  * 執行指令 `update user set password=PASSWORD("你的密碼") where User='root';` 設定密碼
  * 執行指令 `flush privileges;` 刷新 MySQL
  * 執行指令 `quit` 離開 MySQL

> 注意！設置密碼時，要記得加上引號，假設密碼為 1234，應該為:  
> `update user set password=PASSWORD("1234") where User='root';`  
> 以上參考: [http://stackoverflow.com/questions/6474775/setting-the-mysql-root-user-password-on-osx](http://stackoverflow.com/questions/6474775/setting-the-mysql-root-user-password-on-osx)