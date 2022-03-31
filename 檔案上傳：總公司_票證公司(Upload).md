# 檔案上傳：總公司_票證公司(Upload)
###### tags: `資料夾說明文件`

## 上傳BAD檔及交易檔
> CPS 與票證公司所產生的清分清算檔案進行比對後，所產生有帳差的資料，CPS 須將有帳差的資料依票證公司所提供的檔案格式彙整為 BAD 檔，並將原始交易檔一併上傳至票證公司再次進行清分及清算作業。

#### C:\TCPS\FTP_ROOT\
- BAD ：CPS 與 T2 , F2 , TLD 比對後，會在此資料夾產生 BAD 檔及原始交易檔。
- BAD_UPLOAD：上傳 BAD 檔時，，CPS 會將 BAD 檔及原始交易檔壓縮成一個壓縮檔，並放在此資料夾下
- BAD_UPLOAD.BAK：完成壓縮作業後，將 BAD 檔搬移至BAD_UPLOAD.BAK下

![](https://i.imgur.com/qx2f4HJ.jpg)

## 上傳BCD檔
>CPS 每日下載票證公司所產生的結帳交易檔(T2 , F2)進行比對及紀錄帳務資料，若公車業者所設定之業者代碼、路線編號、站別代碼、駕駛員編號及車號有異常時，可以利用 BCD 功能來進行調整。
>一般業者可以修改路線編號、站別代碼、駕駛員編號及車號。
小型業者可以修改路線編號、駕駛員編號及車號。

- 使用者透過 CPS 介面功能：「帳務作業-帳務資料異動」修改帳務資料後，CPS 先將資料儲存於資料庫中。
- 使用者執行上傳 BCD 功能，或是系統自動執行上傳 BCD 檔時間，CPS 讀取存放在資料庫中的資料，寫入 BCD 檔中，並修改帳務資料所對應的 BCD 檔名

#### C:\TCPS\FTP_ROOT\
- BCD_UPLOAD ：CPS 產生的 BCD 檔，透過 FTP 將 BCD 檔上傳至票證公司
- BCD_UPLOAD.BAK：上傳成功後將 BCD 檔搬移至此

![](https://i.imgur.com/03uyzBp.jpg)


## 上傳BCL檔
>目前業者可以針對路線名稱，路線屬性及路線總段次進行維護，在修改後，透過 BCL 的檔案格式上傳至票證公司，進行路線屬性維護作業。


- 使用者透過 CPS 介面功能：「營運參數查詢-路線維護」修改路線基本資料後，CPS 先將資料儲存於資料庫中。
- 使用者執行上傳 BCL 功能，CPS 讀取存放在資料庫中的資料，寫入 BCL 檔中，並修改資料庫路線基本資料所對應的 BCL 檔名。

#### C:\TCPS\FTP_ROOT\
- BCD_UPLOAD：CPS所產生的BCL檔，並透過 FTP 將 BCL 檔上傳至票證公司 Ftp Server
- BCD_UPLOAD.BAK：上傳成功後將 BCD 檔搬移至此

![](https://i.imgur.com/HdLB1Js.jpg)
