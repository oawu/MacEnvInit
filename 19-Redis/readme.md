# 安裝 Redis

## 安裝方法有兩種：
  
  1. 指令安裝(推薦)
  2. 步驟安裝

## 指令安裝(推薦)

  * 終端機執行指令 `brew install redis`

## 步驟安裝(不推薦，因為步驟複雜了點)
  
  * 下載檔案，終端機執行指令 `wget http://download.redis.io/releases/redis-3.0.5.tar.gz`
  * 解開壓縮，執行指令 `tar xzf redis-3.0.5.tar.gz`
  * 進去資料夾，執行指令 `cd redis-3.0.5`
  * 執行指令 `./configure`
  * 執行指令 `make`
  * 執行指令 `sudo make install`

## 啟動 Redis

  * 啟動 Server 終端機執行指令 `redis-server`
  * 啟動 Client 終端機執行指令 `redis-cli`

## WEB 介面
  
  * 使用 [phpRedisAdmin](https://github.com/erikdubbelboer/phpRedisAdmin)。
  * 在 Server 目錄下 clone 專案 `git clone https://github.com/ErikDubbelboer/phpRedisAdmin.git`
  * 進入專案 `cd phpRedisAdmin`
  * 終端機執行指令 `git clone https://github.com/nrk/predis.git vendor`

> 要注意是否有開啟 Redis Server

## 設定

  * 修改檔案 `phpRedisAdmin/includes/config.sample.inc.php`
  * 以下為參考

```
$config = array(
'servers' => array(
  array(
    'name' => 'local server',
    'host' => '127.0.0.1',
    'port' => 6379,
    'filter' => '*',
    'db'   => 0,
    .....
```

## 以上參考

  * [Redis | OA's 常用設定](https://comdan66.github.io/configs/book/mds/mac/redis.html)