# Sublime Text 2
* 下載 - [https://www.sublimetext.com/2](https://www.sublimetext.com/2)
* 把它移到應用程式資料夾，並開啟

## 啟用 Packages
* 網站介紹 - [https://packagecontrol.io/installation#st2](https://packagecontrol.io/installation#st2)
* 打開 Sublime Text 2，按下 `ctrl + esc`
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
	* 下載 [OA.tmTheme](OA.tmTheme) 與 [Theme - OA.zip](Theme - OA.zip)
	* 將 **Theme - OA.zip** 解開壓縮，
	* 點擊左上 `Sublime Text 2` > `preferences` > `Browser Packages..` 後出現一個資料夾
	* 將資料夾 **Theme - OA** 複製到這個資料夾內(沒意外會在 Theme - Default 下面)
	* 將 **OA.tmTheme** 複製到 `Color Scheme - Default` 裡面

## 環境設定
* 快捷鍵 `command + ,`
* 將內容改為以下

``` json
{
	"color_scheme": "Packages/Color Scheme - Default/OA.tmTheme",
	"font_face": "Hack",
	"font_options":
	[
		"no_bold",
		"no_italic",
		"",
		"gray_antialias",
		"subpixel_antialias",
		"no_round"
	],
	"font_size": 21.0,
	"ignored_packages":
	[
		"Vintage"
	],
	"tab_size": 2,
	"theme": "OA.sublime-theme",
	"translate_tabs_to_spaces": true,
	"word_wrap": false
}
```

## 快捷鍵設定
* 點擊左上 `Sublime Text 2` > `preferences` > `Key Bindings - User`
* 將內容改為以下

``` json
[
  {"keys": ["super+l"], "command": "insert", "args": {"characters": "background-color: rgba(0, 0, 255, 0.2);"}},
  {"keys": ["super+i"], "command": "insert_snippet", "args": {"contents": "@include $0;"}},
  {"keys": ["super+r"], "command": "revert" },
  {"keys": ["super+Shift+b"], "command": "insert_snippet", "args": {"contents": "echo '<meta http-equiv=\"Content-type\" content=\"text/html; charset=utf-8\" /><pre>';\r\nvar_dump($0);\r\nexit();"}},
  {"keys": ["super+Shift+g"], "command": "insert_snippet", "args": {"contents": "gg($0);"}},
  {"keys": ["super+Shift+x"], "command": "insert_snippet", "args": {"contents": "console.error($0);\n"}},
  {"keys": ["super+Shift+v"], "command": "insert", "args": {"characters": "border: 1px solid rgba(255, 0, 0, .3);"}},
  {"keys": ["super+Shift+o"], "command": "insert_snippet", "args": {"contents": "@include overflow-docx3();"}},
  {"keys": ["super+o"], "command": "insert_snippet", "args": {"contents": "@include opacity($0);"}},
  {"keys": ["super+Shift+l"], "command": "insert_snippet", "args": {"contents": "@include clearfix();\n"}},
  {"keys": ["super+Shift+j"], "command": "insert_snippet", "args": {"contents": "@include transition($0 .3s);\n"}},
  {"keys": ["super+Shift+s"], "command": "insert_snippet", "args": {"contents": "@include box-shadow($0);\n"}},
  {"keys": ["super+Shift+r"], "command": "insert_snippet", "args": {"contents": "@include range-width($0);"}},
  {"keys": ["super+control+a"], "command": "insert_snippet", "args": {"contents": "<a href='$0' target='_blank'>"}},
  {"keys": ["super+control+z"], "command": "insert_snippet", "args": {"contents": "</a>$0"}},
  {"keys": ["super+control+b"], "command": "insert_snippet", "args": {"contents": "<b>$0</b>"}},
  {"keys": ["super+control+f"], "command": "insert_snippet", "args": {"contents": "function($0) {}"}},
  {"keys": ["super+,"], "command": "insert_snippet", "args": {"contents": "<?php echo $0;?>"}},
  {"keys": ["super+Shift+a"], "command": "insert_snippet", "args": {"contents": "[$0]"}},
  {"keys": ["super+Shift+m"], "command": "insert_snippet", "args": {"contents": "\\M\\"}}
]
```

## 安裝指令
* 打開終端機，輸入指令 `ln -s "/Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`

## 授權
* 打開 Gmail，搜尋 `sublime license`，複製授權碼
* 點擊上方 `Help` > `Enter License`，貼上授權碼