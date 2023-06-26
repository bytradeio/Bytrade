
## /allmarkets
```text
None
```

#### api URL
> https://spot.bytrade.io/open/cmc/allmarkets

#### Method
> GET

#### Content-Type
> none

#### Success Response
```javascript
{
	"code": 0,
	"code_num": 0,
	"msg": "ok",
	"message": "ok",
	"data": [
		{
			"base_currency": "USDT",
			"base_volume": "250346.15610000",
			"highest_bid": "1904.19000000",
			"highest_price_24h": "1910.00000000",
			"last_price": "1904.19000000",
			"lowest_ask": "1904.20000000",
			"lowest_price_24h": "1876.65000000",
			"price_change_percent_24h": "0.843",
			"quote_currency": "ETH",
			"quote_volume": "474661114.10803600",
			"trading_pairs": "ETH-USDT"
		}
	]
}
```
Name | Example            | Type    | Description
--- |--------------------|---------| ---
code | 0                  | Integer |
code_num | 0                  | Integer |
msg | ok                 | String  |
message | ok                 | String  |
data | -                  | Array   |
data.base_currency | USDT               | String  |
data.base_volume | 250346.15610000    | String  |
data.highest_bid | 1904.19000000      | String  |
data.highest_price_24h | 1910.00000000      | String  |
data.last_price | 1904.19000000      | String  |
data.lowest_ask | 1904.20000000      | String  |
data.lowest_price_24h | 1876.65000000      | String  |
data.price_change_percent_24h | 0.843              | String  |
data.quote_currency | ETH                | String  |
data.quote_volume | 474661114.10803600 | String  |
data.trading_pairs | ETH-USDT           | String  |
## /allticker
```text
None
```

#### api URL
> https://spot.bytrade.io/open/cmc/allticker

#### Method
> GET

#### Content-Type
> none

#### 成功响应示例
```javascript
{
	"code": 0,
	"code_num": 0,
	"msg": "ok",
	"message": "ok",
	"data": [
		{
			"UNI-USDT": {
				"base_volume": "412278.64000000",
				"isFrozen": 1,
				"last_price": "5.06400000",
				"quote_volume": "2087456.04343000"
			}
		}
	]
}
```
Name | Example            | Type    | Description
--- | --- | --- | ---
code | 0 | Integer |
code_num | 0 | Integer |
msg | ok | String |
message | ok | String |
data | - | Array |
data.UNI-USDT | - | Object |
data.UNI-USDT.base_volume | 412278.64000000 | String |
data.UNI-USDT.isFrozen | 1 | Integer |
data.UNI-USDT.last_price | 5.06400000 | String |
data.UNI-USDT.quote_volume | 2087456.04343000 | String |
## /orderbook/market_pair
```text
None
```

#### api URL
> https://spot.bytrade.io/open/cmc/orderbook/market_pair?market_pair=BTC-USDT&depth=50

#### Method
> GET

#### Content-Type
> none

#### Query Parameters
Name | Example            | Type  |  Mandatory | Description
--- | --- | --- | -- | ---
market_pair | BTC-USDT | String | Yes | -
depth | 50 | Integer | Yes | -

#### Success Response
```javascript
{
    "code": 0,
        "code_num": 0,
        "msg": "ok",
        "message": "ok",
        "data": {
            "asks": [
                [
                    "30643.94000000",
                    "5.09805000"
                ]
            ], 
            "bids": [
                [
                    "30643.93000000",
                    "0.68136000"
                ]
            ],
            "timestamp": 1687661633
    }
}
```
Name | Example            | Type  | Description
--- | --- | --- | ---
code | 0 | Integer |
code_num | 0 | Integer |
msg | ok | String |
message | ok | String |
data | - | Object |
data.asks | - | Array | asks
data.asks.0 | 27170.18000000 | String | quantity
data.asks.1 | 0.93741000 | String | price
data.bids | - | Array | bids
data.bids.0 | 27170.17000000 | String | quantity
data.bids.1 | 7.59207000 | String | price
data.timestamp | 1685778768 | Integer |
## //trades/market_pair
```text
None
```

#### api URL
> https://spot.bytrade.io/open/cmc/trades/market_pair?market_pair=BTC-USDT

#### Method
> GET

#### Content-Type
> none

#### Query Parameters
Name | Example            | Type  |  Mandatory | Description
--- | --- | --- | -- | ---
market_pair | BTC-USDT | String | Yes | -

#### Success Response
```javascript
{
	"code": 0,
	"code_num": 0,
	"msg": "ok",
	"message": "ok",
	"data": [
		{
			"base_volume": "13.3134372",
			"price": "27170.28000000",
			"quote_volume": "0.00049000",
			"timestamp": 1685778941711,
			"trade_id": 3132644023,
			"type": "sell"
		}
	]
}
```
Name | Example            | Type | Description
--- | --- | --- | ---
code | 0 | Integer |
code_num | 0 | Integer |
msg | ok | String |
message | ok | String |
data | - | Array |
data.base_volume | 13.3134372 | String |
data.price | 27170.28000000 | String |
data.quote_volume | 0.00049000 | String |
data.timestamp | 1685778941711 | Integer |
data.trade_id | 3132644023 | Integer |
data.type | sell | String |

## /assets
```text
None
```

#### api URL
> https://spot.bytrade.io/open/cmc/assets

#### Method
> GET

#### Content-Type
> none
> 
#### Success Response
```javascript
{
	"code": 0,
	"code_num": 0,
	"msg": "ok",
	"message": "ok",
	"data": {
		"ADA": {
			"can_deposit": true,
			"can_withdraw": true,
			"maker_fee": "0.006",
			"max_withdraw ": "2000",
			"min_withdraw": "20",
			"name": "ADA",
			"taker_fee": "0.006",
			"unified_cryptoasset_id": 0, 
            "contractAddressUrl": "https://bscscan.com/address/0x3ee2200efb3400fabb9aacf31297cbdd1d435d47",
            "contractAddress": "0x3ee2200efb3400fabb9aacf31297cbdd1d435d47"
		}
	}
}
```
 Name                           | Example | Type    | Description
--------------------------------|---------|---------| ---
 code                           | 0       | Integer |
 code_num                       | 0       | Integer |
 msg                            | ok      | String  |
 message                        | ok      | String  |
 data                           | -       | Object  |
 data.ADA                       | -       | Object  |
 data.ADA.can_deposit           | true    | Boolean |
 data.ADA.can_withdraw          | true    | Boolean |
 data.ADA.maker_fee             | 0.006   | String  |
 data.ADA.max_withdraw          | 2000    | String  |
 data.ADA.min_withdraw          | 20      | String  |
 data.ADA.name                  | ADA     | String  |
 data.ADA.taker_fee             | 0.006   | String  |
 data.ADA.unified_cryptoasset_id | 0       | Integer | 
 data.ADA.contractAddressUrl | -       | String  |
 data.ADA.contractAddress | -       | String  |
