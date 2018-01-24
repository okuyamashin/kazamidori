# kazamidori
This project provides BTC log files formatted csv.  

## format description  
### bitflyer.jp daily ticker log format  

|fields|description|
|:---|:---|
|domain|Fixed value "bitflyer.jp"|
|product_code|Type of currency pair like "BTC_JPY"|
|health|The health status of bitflyer.jp servers.|
|status|Status of acceptance orders|
|loaded|Our server timestamp rounded minutes|
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


