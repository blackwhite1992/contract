# DRStock

## contract

dev endpoint: `http://18.180.227.173:8545/`

### DRStock `0xD25066df53806c8f79F9D9BBECd22D91a91Bb112`

**Function**
        
-buyStock(                        //购买股票
        address payable account,  //购买者地址
        uint256 amount,           //总金额
        uint256 nonce,            //nonce
        string memory stockCode,  //股票代码
        string memory unitPrice,  //单价
        uint8 expires,            //期限 15天/30天
        uint8 status,             //状态 0做空 1做多
        uint8 v,                  //v
        bytes32 r,                //r
        bytes32 s                 //s
    )

- nonceOf(address): 获取某个地址的nonce值
    * address: 输入地址


    

- adminClaim(address payable account,   //接收地址
               uint256 amount)          //提取金额
                            
                            
//根据索引获取投资者信息
-getInvestor(uint256 index)   //投资索引
