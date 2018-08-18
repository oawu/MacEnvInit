# 安裝 Memcached

## 安裝方法有兩種：
  1. 指令安裝(推薦)
  2. 步驟安裝

## 指令安裝(推薦)
  
  * 指令 `brew install memcached`

## 步驟安裝(不推薦，因為步驟複雜了點)
  
  * Memcached 相依於 **libevent**, 所以在安裝之前要先安裝 [libevent](http://libevent.org)。

  * 安裝 libevent
    * 選擇暫存資料夾 `cd /tmp`
    * 下載檔案 `wget https://github.com/downloads/libevent/libevent/libevent-2.0.18-stable.tar.gz`
    * 解開壓縮 `tar zxvf libevent-2.0.18-stable.tar.gz`
    * 進去資料夾 `cd libevent-2.0.18-stable`
    * 執行指令 `./configure`
    * 執行指令 `make`
    * 執行指令 `sudo make install`

  * 安裝 Memcached
    * 選擇暫存資料夾 `cd /tmp`
    * 下載檔案 `wget http://memcached.googlecode.com/files/memcached-1.4.13.tar.gz`
    * 解開壓縮 `cd memcached-1.4.13`
    * 執行指令 `./configure`
    * 執行指令 `make`
    * 執行指令 `sudo make install`

## 啟動 Memcached
  
  * 啟動指令 `memcached -p 8000`，`-p` 代表 **port**。
  * 背景執行指令 `memcached -d -p 8000`，加個 `-d` 即可背景。

## WEB 介面
  
  * 使用(推薦) [memcache.php_ByHarunYayli](https://github.com/comdan66/memcache.php_ByHarunYayli)
  * 使用 [phpMemAdmin](https://github.com/clickalicious/phpmemadmin)
  * 使用 [memcached](https://github.com/memcached/memcached)
  * 使用 [phpMemcacheAdmin](https://github.com/hgschmie/phpmemcacheadmin)

## 以上參考
  
  * [Install Memcached on Mac OS X](https://www.hacksparrow.com/install-memcached-on-mac-os-x.html)