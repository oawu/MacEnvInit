# 設定 Host

  * 位置在 `/etc/hosts`
  * 為了之後方便常常設定，不用每次輸入密碼，終端機執行指令 `sudo chmod 777 /etc/hosts` 將權限打開
  * 為了之後方便常常設定，所以建立一個鏈結，終端機執行指令 `ln -s /etc/hosts /Users/oa/Documents/hosts`

## 常用設定如下

```
127.0.0.1 dev.case.ioa.tw
```



# 設定 Virtual Host
  * 位置在 `/usr/local/etc/httpd/extra/httpd-vhosts.conf`
  * 為了之後方便常常設定，不用每次輸入密碼，開啟終端機，輸入指令 `sudo chmod 777 /usr/local/etc/httpd/extra/httpd-vhosts.conf` 將權限打開
  * 為了之後方便常常設定，所以建立一個鏈結，開啟終端機，輸入指令 `ln -s /usr/local/etc/httpd/extra/httpd-vhosts.conf /Users/oa/Documents/httpd-vhosts.conf`

## 常用設定如下

```
# root
<VirtualHost *:80>
  ServerAdmin comdan66@gmail.com
  DocumentRoot "/Users/OA/www"

  <Directory "/Users/OA/www">
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

  DocumentRoot "/Users/OA/www/case"
  <Directory "/Users/OA/www/case">
      Options FollowSymLinks MultiViews
      AllowOverride All
      Order allow,deny
      Allow from all
  </Directory>
</VirtualHost>

# Zeus
<VirtualHost *:443>
    DocumentRoot "/Users/OA/www/zeusdesign/zeusdesign_admin
    ServerName dev.admin.zeusdesign.com.tw
    SSLEngine on
    SSLCertificateFile "/usr/local/etc/httpd/server.crt"
    SSLCertificateKeyFile "/usr/local/etc/httpd/server.key"
</VirtualHost>
<VirtualHost *:80>
  ServerName  dev.admin.zeusdesign.com.tw
  ServerAlias  dev.admin.zeusdesign.com.tw

  DocumentRoot "/Users/OA/www/zeusdesign/zeusdesign_admin"
  <Directory "/Users/OA/www/zeusdesign/zeusdesign_admin">
      Options FollowSymLinks MultiViews
      AllowOverride All
      Order allow,deny
      Allow from all
  </Directory>
</VirtualHost>
```