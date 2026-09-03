# JJClab_HW5
參考筆記: https://github.com/wsunccake/sle15_notes/blob/master/practice/ch2.md

---------------------
# 練習 3. 文字處理工具（cat / grep / head / tail / more / less）  
  ## 3-1. 建立並查詢 log.txt
  創建week4資料夾以利作業，接著利用cat將指定內容寫入log.txt，再以cat log.txt顯示其內容。  
  
  <img width="431" height="564" alt="image" src="https://github.com/user-attachments/assets/712858b4-bf0f-4a7e-a508-8408c33b1676" />

  |題號|描述|指令|
  |------------|------------|------------|
  |3-1-3|顯示全部內容，並顯示行號| cat -n log.txt 或 nl log.txt|
  |3-1-4|只顯示前 3 行|head -n 3 log.txt|
  |3-1-5|只顯示最後 3 行|tail -n 3 log.txt|
  |3-1-6|找出所有含 ERROR 的行|grep ERROR log.txt|
  |3-1-7|找出所有不是 INFO 的行|grep -v INFO log.txt|

  以上小題執行結果: 
  
  <img width="499" height="539" alt="image" src="https://github.com/user-attachments/assets/7347284f-cd8d-47ce-b262-a27e8bf085bf" />

  ## 3-2. 持續顯示系統日誌
  tail -f 的意義: 不只是顯示檔案最後幾行，而是持續等待新內容。

  開啟第二個terminal，嘗試創造一些log，再用第一Terminal監控。

  第一terminal如下圖: 

  <img width="801" height="794" alt="image" src="https://github.com/user-attachments/assets/be37bc90-936f-4ddf-b2d2-2f17f2c34f44" />

  在第二terminal嘗試登入root，並故意失敗  

  <img width="800" height="795" alt="image" src="https://github.com/user-attachments/assets/2b91dd28-314f-4735-87bb-431b8736b35c" />

  第一terminal確實追蹤登入失敗訊息: 

  <img width="802" height="795" alt="image" src="https://github.com/user-attachments/assets/b432b34f-5883-4dd5-9f68-d8b0da546fad" />

  ## 3-3：過濾 SSH 設定檔
  這裡的 grep -v表示反向選擇，將符合條件的隱藏顯示。完整指令執行後如下圖:  

  <img width="794" height="215" alt="image" src="https://github.com/user-attachments/assets/bef40b48-0b3d-4e41-8e89-06d9893bff1f" />

  < ^\s*(#|$) >篩選條件為: 
  |------------|------------|
  |^       | 一行開頭
  |\s*     | 允許前面有空白
  |#       | 註解
  |"|"     | 或
  |$       | 空白行/行尾

  舉例，若移除空白行篩選，結果如下:  
  <img width="674" height="758" alt="image" src="https://github.com/user-attachments/assets/0f320968-d560-44ef-a66c-5dfa09a3d72d" />
