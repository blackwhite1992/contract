
### 端口
20225

### 通用响应
```json
    {
   "code": 200,
   "message": "",
   "result": {}
    }
```

### 异常响应
```json
    {
  "code": 400,
  "message": "The claim data error",
  "result": null
}
```

### 购买stock  
POST /api/buyStock 

req
```json
{
  "account": "string",
  "chainId": "string",
  "expires": 0,     //到期时间 15天 30天
  "nonce": 0,
  "number": 0,      //购买数量 100的倍数
  "state": 0,      // 0做空 1做多
  "stockCode": "string",    //股票代码
  "totalPrice": 0,          //总价
  "unitPrice": "string"     //单价
}
```

res
```json
{
  "code": 200,
  "message": "OK",
  "result": {
    "account": "1",
    "stockCode": "1",
    "unitPrice": "0",
    "totalPrice": "0",
    "expires": "15",
    "state": "0",
    "nonce": "1",
    "v": "27",
    "r": "0x96718ce3674d353456cc8b7fc1993ee0065bbf07fe0c54ea90a0e3b21f6a037a",
    "s": "0x3dfdfa07585e39fe5dafbc0c8e33b756e51ef716e2a74cda48338a47084ecc47"
  }
}
```

### 获取链信息
GET /api/chains

res
```json
{
  "code": 200,
  "message": "OK",
  "result": [
    {
      "chainId": "0x7b",
      "coin": "BNB",
      "rpcUrls": [
        "http://18.180.227.173:8545"
      ],
      "chainName": "BSC",
      "defaultFlag": true,
      "contract": "0x6B10C8648bbf7505fE3e42090a268E13a43E9FdE"
    }
  ]
}
```

### 用户取钱
POST  /api/getFundClaim

req
```json
{
  "account": "1",
  "chainId": "1",
  "index": 0,   //股票链index
  "nonce": 0,
  "stockCode": "1"
}
```

res
```json
{
  "code": 200,
  "message": "OK",
  "result": {
    "account": "1",
    "amount": "1",
    "nonce": "0",
    "v": "27",
    "r": "0x4e4195e8518a083c27bad6b3e5808c756acca47e260808b9782d21f21981cce6",
    "s": "0x1adeb12bb506ebdb469316d4315a9c7d891f04cb4385cd34232647902f5e696d"
  }
}
```

### 获取可用余额
GET /api/getStockAmount

req
|参数|类型|备注|
|:-:|:-:|:-:|
|`stockCode `|`string`|股票代码|

res
```json
{
  "code": 200,
  "message": "OK",
  "result": {
    "stockCode": "10001",
    "amount": "20000"
  }
}
```

### 根据股票代码和时间查询价格信息
GET /api/getStockInfo

req
|参数|类型|备注|
|:-:|:-:|:-:|
|`stockCode `|`string`|股票代码|
|`days `|`integer`|天数 15天 30天|

res
```json
{
  "code": 200,
  "message": "OK",
  "result": {
    "name": [
      "特锐德",
      "300001.sz"
    ],
    "now_price": 14.9500000001,
    "days": 30,             //时间 15天 30天
    "theoretical": 5.3575   //期权费
  }
}
```

### 用户平仓
POST /api/sellStock

req
```json
{
  "account": "1",     
  "closePrice": "1",    //平仓价格
  "stockCode": "1", 
  "stockId": 0          //股票链index
}
```


res
```json
{
    "code": 200,
   "message": "",
   "result": {}
    }
```


