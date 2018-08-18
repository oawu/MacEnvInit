# 安裝 PHP 語言

## 安裝前準備

  * 請先安裝 [Apache](../12-Apache/)

## 安裝各版本的 PHP

  * 安裝 PHP 5.6 版本 `brew install php@5.6`
  * 安裝 PHP 7.0 版本 `brew install php@7.0`
  * 安裝 PHP 7.1 版本 `brew install php@7.1`
  * 安裝 PHP 最新 版本 `brew install php`

## Cli 指令模式設定
  * 用 Sublime Text 2 打開編輯 `~/.zshrc`，終端機執行指令 `subl ~/.zshrc`
  * 稍微檢查一下以下路徑是否存在後在檔案最後方新增以下內容

```
## PHP 5.6
#export PATH="/usr/local/opt/php@5.6/bin:$PATH"
#export PATH="/usr/local/opt/php@5.6/sbin:$PATH"

## PHP 7.0
#export PATH="/usr/local/opt/php@7.0/bin:$PATH"
#export PATH="/usr/local/opt/php@7.0/sbin:$PATH"

## PHP 7.1
#export PATH="/usr/local/opt/php@7.1/bin:$PATH"
#export PATH="/usr/local/opt/php@7.1/sbin:$PATH"

## PHP 7
#export PATH="/usr/local/opt/php/bin:$PATH"
#export PATH="/usr/local/opt/php/sbin:$PATH"
```
  
  * **Cli** 要切換版本的話，就把 `~/.zshrc` 該版的註解拿掉
  * 然後終端機執行指令 `source ~/.zshrc`

## Apache 模式設定
  * 用 Sublime Text 2 打開編輯 `/usr/local/etc/httpd/httpd.conf`，終端機執行指令 `subl /usr/local/etc/httpd/httpd.conf`
  * 稍微檢查一下以下路徑是否存在後在檔案最後方加入以下內容

```
#LoadModule php5_module /usr/local/opt/php@5.6/lib/httpd/modules/libphp5.so
#LoadModule php7_module /usr/local/opt/php@7.0/lib/httpd/modules/libphp7.so
#LoadModule php7_module /usr/local/opt/php@7.1/lib/httpd/modules/libphp7.so
#LoadModule php7_module /usr/local/opt/php@7.2/lib/httpd/modules/libphp7.so
```
  * 若要更換版本，就把 **LoadModule** 該版本註解拿掉後，重開 Apache 即可

## 設定 Apache 讀取執行 PHP

  * 用 Sublime Text 2 打開編輯 `/usr/local/etc/httpd/httpd.conf`，終端機執行指令 `subl /usr/local/etc/httpd/httpd.conf`，修改以下內容

```
<IfModule dir_module>
  DirectoryIndex index.html
</IfModule>
```

```
<IfModule dir_module>
  DirectoryIndex index.php index.html
</IfModule>

<FilesMatch \.php$>
  SetHandler application/x-httpd-php
</FilesMatch>
```
  * 重開 Apache，終端機執行指令 `sudo apachectl -k restart`

## 各版本的 php.ini
  
  * PHP 5.6 版本 - `/usr/local/etc/php/5.6/php.ini`
  * PHP 7.0 版本 - `/usr/local/etc/php/7.0/php.ini`
  * PHP 7.1 版本 - `/usr/local/etc/php/7.1/php.ini`
  * PHP 7.2 版本 - `/usr/local/etc/php/7.2/php.ini`

## 安裝 imagick
  * 先要安裝 **imagemagick**，終端機執行指令 `brew install imagemagick`
  * :exclamation: 請先將 Cli 的 php 切換到指定的版本，可以用 `php -v` 檢查目前 Cli 的 php 版本
  * 終端機執行指令 `pecl install imagick`，中間有個 `Please provide the prefix of Imagemagick installation [autodetect]`，直接按 `enter` 即可
  * 結果若是失敗如果出現 `configure: error: Please reinstall the pkg-config distribution`，那就終端機執行指令 `brew reinstall pkg-config` 後再執行 `pecl install imagick` 即可
  * 檢查該版本的 `php.ini` 內是否有 `extension="imagick.so"`
  * Cli 下要找 php.ini 位置，終端機執行指令 `php --ini` 即可
  * 完成後重開 Apache，終端機執行指令 `sudo apachectl -k restart`，然後看 `phpinfo()` 是否有 `imagick`

## 安裝 redis
  * 先要安裝 **redis**，終端機執行指令 `brew install redis`
  * :exclamation: 請先將 Cli 的 php 切換到指定的版本，可以用 `php -v` 檢查目前 Cli 的 php 版本
  * 終端機執行指令 `pecl install redis`，中間有個 `enable igbinary serializer support? [no] :` 與 `enable lzf compression support? [no] :`，都直接按 `enter` 即可
  * 結果若是失敗如果出現 `configure: error: Please reinstall the pkg-config distribution`，那就終端機執行指令 `brew reinstall pkg-config` 後再執行 `pecl install redis` 即可
  * 檢查該版本的 `php.ini` 內是否有 `extension="redis.so"`
  * Cli 下要找 php.ini 位置，終端機執行指令 `php --ini` 即可
  * 完成後重開 Apache，終端機執行指令 `sudo apachectl -k restart`，然後看 `phpinfo()` 是否有 `redis`

## 安裝 Deployer 部署器
  
  * 終端機執行指令 `curl -LO https://deployer.org/deployer.phar`
  * 終端機執行指令 `mv deployer.phar /usr/local/bin/dep`
  * 終端機執行指令 `chmod +x /usr/local/bin/dep`
  * 檢查是否安裝成功，重新開啟終端機，執行指令 `dep -v`

## 安裝 Composer 套件管理
  
  * 終端機執行指令 `php -r "readfile('https://getcomposer.org/installer');" > composer-setup.php`
  * 終端機執行指令 `php composer-setup.php`
  * 終端機執行指令 `php -r "unlink('composer-setup.php');"`
  * 終端機執行指令 `mv composer.phar /usr/local/bin/composer`
  * 檢查是否安裝成功，重新開啟終端機，執行指令 `composer -v`
  
## 重點整理

  * PHP 5.6 版本 ini 檔案 - `/usr/local/etc/php/5.6/php.ini`
  * PHP 7.0 版本 ini 檔案 - `/usr/local/etc/php/7.0/php.ini`
  * PHP 7.1 版本 ini 檔案 - `/usr/local/etc/php/7.1/php.ini`
  * PHP 7.2 版本 ini 檔案 - `/usr/local/etc/php/7.2/php.ini`
  * Apache 若要更換版本，就用 Sublime Text 2 打開編輯 `/usr/local/etc/httpd/httpd.conf`，終端機執行指令 `subl /usr/local/etc/httpd/httpd.conf`，把 **LoadModule** 該版本註解拿掉後，重開 Apache 即可
  * Cli 要切換版本的話，就用 Sublime Text 2 打開編輯 `~/.zshrc`，終端機執行指令 `subl ~/.zshrc`，把要的版本註解拿掉，然後終端機執行指令 `source ~/.zshrc` 即可
