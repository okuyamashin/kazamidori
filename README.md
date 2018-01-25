# KAZAMIDORI
This project provides BTC log files formatted csv.  

## Format description  
### bitflyer.jp daily ticker log format  
file name : bitflyer.ticker.[YMD].[PRODUCT CODE].csv.gz

|fields|description|
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

