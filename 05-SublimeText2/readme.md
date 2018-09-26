# 安裝 Sublime Text 2 文字編輯器
  
  * 官網下載 - [https://www.sublimetext.com/2](https://www.sublimetext.com/2)
  * 備用載點 - (Sublime Text 2.0.2.dmg)[https://cdn.ioa.tw/MacEnvInit/Sublime+Text+2.0.2.dmg]
  * 把它移到**應用程式資料夾**，並開啟

## 啟用 Packages
  
  * 網站介紹 - [https://packagecontrol.io/installation#st2](https://packagecontrol.io/installation#st2)
  * 打開 Sublime Text 2，按下 `ctrl + ~`
  * 輸入以下後按 Enter

``` python
import urllib2,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```
  * 重新開啟 Sublime Text 2

## 安裝套件

  * SublimeLinter
    * 打開 Sublime Text 2，按下 `command + shift + p`
    * 輸入 `install` 選擇 `Package Control: Install Package`
    * 接著輸入 `SublimeLinter`，選擇 `SublimeLinter`
    * 重新開啟 Sublime Text 2

  * Scss
    * 打開 Sublime Text 2，按下 `command + shift + p`
    * 輸入 `install` 選擇 `Package Control: Install Package`
    * 接著輸入 `SCSS`，選擇 `SCSS`
    * 重新開啟 Sublime Text 2

## 主題

  * 下載 [OA.tmTheme](https://cdn.ioa.tw/MacEnvInit/OA.tmTheme) 與 [Theme - OA.zip](https://cdn.ioa.tw/MacEnvInit/Theme - OA.zip)
  * 將 **Theme - OA.zip** 解開壓縮，
  * 點擊左上 `Sublime Text 2` > `preferences` > `Browser Packages..` 後出現一個資料夾
  * 將資料夾 **Theme - OA** 複製到這個資料夾內(沒意外會在 Theme - Default 下面)
  * 將 **OA.tmTheme** 複製到 `Color Scheme - Default` 裡面

## 環境設定
  
  * 點擊左上 `Sublime Text 2` > `preferences` > `Browser Packages..` 後出現一個資料夾
  * 進入資料夾 `User`
  * 下載 [Preferences.sublime-settings](https://cdn.ioa.tw/MacEnvInit/Preferences.sublime-settings)
  * 將下載的檔案複製到 `User` 資料夾，將原本的 `Preferences.sublime-settings` 取代

## 快捷鍵設定
  
  * 點擊左上 `Sublime Text 2` > `preferences` > `Browser Packages..` 後出現一個資料夾
  * 進入資料夾 `User`
  * 下載 [Default (OSX).sublime-keymap](https://cdn.ioa.tw/MacEnvInit/Default+(OSX).sublime-keymap)
  * 將下載的檔案複製到 `User` 資料夾，將原本的 `Default (OSX).sublime-keymap` 取代
  * 注意！下載下來的檔案是 `Default+(OSX).sublime-keymap`，記得把中間的 `+` 改為 `空格`

## 安裝指令
  
  * 打開 `iTerm2` 終端機，執行指令 `mkdir ~/bin`
  * 打開終端機，輸入指令 `ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/subl`
  * 用 Sublime Text 2 打開編輯 `~/.zshrc`
  * 在檔案最下面新增 `export PATH=$PATH:$HOME/bin`
  * 以上參考 [https://gist.github.com/barnes7td/3804534](https://gist.github.com/barnes7td/3804534)

## 授權

  * 打開 Gmail，搜尋 `sublime license`，複製授權碼
  * 點擊上方 `Help` > `Enter License`，貼上授權碼
