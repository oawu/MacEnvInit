# 指令筆記

  * `pwd` - 顯示目前的位置
  * `which 指令` - 顯示此指令的位置
  * `ln -s 真實檔案 捷徑檔案` - 建立捷徑指令
  * `sudo chown -R oa /檔案/` - 變更擁有者， -R 為全部資料夾

## 關掉 Spotlight 索引
關掉 Spotlight: 如果你完全不使用 Spotlight，則可以考慮把 Spotlight 完全關閉  
而 Spotlight 基本上是沒辦法從圖形介面去關閉的，所以你必須先打開你的終端機輸入一些指令！
  
  * 終端機執行指令 `sudo mdutil -i off /`
  * 終端機執行指令 `sudo mdutil -i off -a`
