# KAZAMIDORI
This project provides BTC log files formatted csv.  
Our server is gathering public data from exchange sites every minutes, 
and will upload csv files every day.  

#### 2018.01.28
We are currenly preparing a web site for information of bit coins and forcast using artifical intelligence.  
[Cyber Kazamidori](https://cyber-kazamidori.jp/)

#### 2018.01.31
Format change  
Volume Minute field is added to Ticker csv file. It is summery of size of executions after privious ticker entry.  

## Format description  
### bitflyer.jp daily ticker log format  
file name : bitflyer.ticker.[YMD].[PRODUCT CODE].csv.gz

|field|description|
|:---|:---|
|domain|Fixed value "bitflyer.jp"|
|product_code|Type of currency pair like "BTC_JPY"|
|health|The health status of bitflyer.jp servers.|
|status|Status of acceptance orders|
|loaded|Our server timestamp rounded minutes formatted yyyy-MM-dd'T'HH:mm:ss.SSSZZ |
|timestamp|Tick timestamp of bitflyer.jp occationally blank value|
|tick_id|Tick id|
|best_bid|Best bid|
|best_ask|Best ask|
|best_bid_size|Best bid size|
|best_ask_size|Best ask size|
|total_bid_depth|Summery of size of bid orders|
|total_ask_depth|Summery of size of ask orders|
|ltp||
|volume||
|volume_by_product||
|last_price|Last execution price|

"health" field takes following values  
NORMAL,BUSY,VERY BUSY,SUPER BUSY,NO ORDER,STOP

"status" field takes following values  
RUNNING,CLOSED,STARTING,PREOPEN,CIRCUIT BREAK,AWAITING SQ,MATURED	

### bitflyer.jp daily execution log format
file name : bitflyer.execution.[YMD].[PRODUCT CODE].csv.gz 

|field|description|
|:---|:---|
|domain|Fixed value "bitflyer.jp"|
|product_code|Type of currency pair like "BTC_JPY"|
|loaded|Our server timestamp|
|id|Trade id|
|exec_date|Execution timestamp occationally blank value coused by mal formatted data of api|
|side|"SELL" or "BUY"|
|price|Execution price|
|size|Size|
|buy_child_order_acceptance_id||
|sell_child_order_acceptance_id||

