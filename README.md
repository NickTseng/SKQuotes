  
  ### 群益懶人報價機 SKQuotes
群益自動收集Tick程式 Automatic Quote Machine. </br>
僅適用於台指期, 目前無股票自動報價功能 </br>
此程式並非用來看盤, 主要用於載tick時做盤中的策略下單

群益 API 官網
<https://www.capital.com.tw/Service2/download/API.asp>

### Working Enviroment 
* Windows 10 Professional (64-bit)</br>
* Microsoft SQL Server 2017 Developer (64-bit)
* 群益API 版本2.13.16, 必要環境輔助安裝工具 (Visual C++ 可轉發套件)

### 提供功能:
1. 程式啟動後會自動做登入動作, 無須操作即可將Tick load到database
2. 自動載入前日分K, 日K資料. 判斷僅用weekday-1, 並無特別使用交易日
3. 使用exe.Config檔參數載入

### 使用方法
1. 安裝SKCOM裡的dll, 右鍵執行install.bat
2. 將程式裡所需要用到的DB還原(https://github.com/hanyang0721/Stock-Database.git)
3. 修改SKQuote.ps1裡面的程式路徑參數, 後在工作排成裡設定8:45與15:00啟用
4. 填入exe.config裡的參數
5. 繼續debug

### 注意事項
* 程式並不會備份歷史tick, 需自行建job備份
* 程式會與報價server斷線如超過一段時間沒有new tick
* 群益API版本必須一致, 否則程式可能開不起來
* 必須有群益期貨帳號, 並且開通 API 使用權限後才能使用(通常為申請API隔日生效)


