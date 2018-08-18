 # 安裝 Apache Http 服務器

  * 更新 xcode command line，終端機下 `xcode-select --install`
  * 更新 Brew `brew update`
  * 移除停止使用 mac 原生的 Apache
    * 先暫停 Apache `sudo apachectl stop`
    * 自動開啟先關閉 `sudo launchctl unload -w /System/Library/LaunchDaemons/org.apache.httpd.plist 2>/dev/null`

  * 安裝新的 Apache
    * 用 Brew 安裝 `brew install httpd`
    * 啟動 Apache `sudo brew services start httpd`
    * 設定 `ps -aef | grep httpd`
    * 重開 `sudo apachectl -k restart`

  * 新 Apache 指令
    * 開啟 `sudo apachectl start`
    * 關閉 `sudo apachectl stop`
    * 重開 `sudo apachectl -k restart`

  * 新 Apache 相關設定
    * 用 Sublime Text 2 打開編輯 `/usr/local/etc/httpd/httpd.conf`，終端機執行指令 `subl /usr/local/etc/httpd/httpd.conf`
    * 修改 `Listen 8080` 改為 `Listen 80`
    * 修改 `DocumentRoot "/usr/local/var/www"`，改成指定位置 `DocumentRoot "/Users/oa/www"`
    * 修改 `<Directory "/usr/local/var/www">`，改成指定位置 `<Directory "/Users/oa/www">`
    * 拿掉註解 `LoadModule rewrite_module lib/httpd/modules/mod_rewrite.so`
    * 拿掉註解，並改成 `ServerName localhost`
    * 拿掉註解 `Include /usr/local/etc/httpd/extra/httpd-vhosts.conf`
    * 為了之後方便常常設定，不用每次輸入密碼，開啟終端機，輸入指令 `sudo chmod 777 /usr/local/etc/httpd/httpd.conf` 將權限打開
    * 為了之後方便常常設定，所以建立一個鏈結，開啟終端機，輸入指令 `ln -s /usr/local/etc/httpd/httpd.conf /Users/oa/Documents/httpd.conf`

  * 重開 Apache `sudo apachectl -k restart`

## 設定 Host

  * 位置在 `/etc/hosts`
  * 為了之後方便常常設定，不用每次輸入密碼，終端機執行指令 `sudo chmod 777 /etc/hosts` 將權限打開
  * 為了之後方便常常設定，所以建立一個鏈結，終端機執行指令 `ln -s /etc/hosts /Users/oa/Documents/hosts`
  * 用 Sublime Text 2 打開編輯 `/etc/hosts`，終端機執行指令 `subl /etc/hosts`，將內容調整一下，常用內容如下：

```
127.0.0.1 dev.case.ioa.tw
```

## 設定 Virtual Host

  * 位置在 `/usr/local/etc/httpd/extra/httpd-vhosts.conf`
  * 為了之後方便常常設定，不用每次輸入密碼，開啟終端機，輸入指令 `sudo chmod 777 /usr/local/etc/httpd/extra/httpd-vhosts.conf` 將權限打開
  * 為了之後方便常常設定，所以建立一個鏈結，開啟終端機，輸入指令 `ln -s /usr/local/etc/httpd/extra/httpd-vhosts.conf /Users/oa/Documents/httpd-vhosts.conf`
  * 用 Sublime Text 2 打開編輯 `/usr/local/etc/httpd/extra/httpd-vhosts.conf`，終端機執行指令 `subl /usr/local/etc/httpd/extra/httpd-vhosts.conf`，將內容調整一下，常用內容如下：

```
# root
<VirtualHost *:80>
  ServerAdmin comdan66@gmail.com
  DocumentRoot "/Users/oa/www"

  <Directory "/Users/oa/www">
      Options FollowSymLinks MultiViews
      AllowOverride All
      Order allow,deny
      Allow from all
  </Directory>
</VirtualHost>

# Case
<VirtualHost *:80>
  ServerName dev.case.ioa.tw
  ServerAlias dev.case.ioa.tw

  DocumentRoot "/Users/oa/www/case"
  <Directory "/Users/oa/www/case">
      Options FollowSymLinks MultiViews
      AllowOverride All
      Order allow,deny
      Allow from all
  </Directory>
</VirtualHost>
```

## 重點整理

  * Conf 位置 `/usr/local/etc/httpd/httpd.conf`
  * Vhosts 位置 `/usr/local/etc/httpd/extra/httpd-vhosts.conf`
  * 開啟 Apache，終端機執行指令 `sudo apachectl start`
  * 關閉 Apache，終端機執行指令 `sudo apachectl stop`
  * 重開 Apache，終端機執行指令 `sudo apachectl -k restart`
