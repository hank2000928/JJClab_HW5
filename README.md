## JJClab_HW5
參考筆記: https://github.com/wsunccake/sle15_notes/blob/master/practice/ch2.md

---------------------
## 練習 3. 文字處理工具（cat / grep / head / tail / more / less）  
  3-1. 建立並查詢 log.txt
  創建week4資料夾以利作業，接著利用cat將指定內容寫入log.txt，再以cat log.txt顯示其內容。  
  
  <img width="431" height="564" alt="image" src="https://github.com/user-attachments/assets/712858b4-bf0f-4a7e-a508-8408c33b1676" />

  ｜題號｜描述｜指令｜
  ｜------------｜------------｜------------｜
  ｜3-1-3｜顯示全部內容，並顯示行號｜ cat -n log.txt 或 nl log.txt｜
  ｜3-1-4｜只顯示前 3 行｜head -n 3 log.txt｜
  ｜3-1-5｜只顯示最後 3 行｜tail -n 3 log.txt｜
  ｜3-1-6｜找出所有含 ERROR 的行｜grep ERROR log.txt｜
  ｜3-1-7｜找出所有不是 INFO 的行	｜grep -v INFO log.txt｜
