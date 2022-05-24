

## DRStock_contract

dev endpoint: `http://18.180.227.173:8545/`

### DRStock `0xD25066df53806c8f79F9D9BBECd22D91a91Bb112`

**Function**
        
# 用户来购买股票
- buyStock(address account,uint256 amount,uint256 nonce,string memory stockCode,string memory unitPrice,uint8 expires,uint8 status,uint8 v,bytes32 r,bytes32 s)
    * account：   购买者地址
    * amount：    总金额
    * nonce：     nonce
    * stockCode： 股票代码
    * unitPrice： 股票单价
    * expires：   期限 15天/30天
    * status:     状态 0做空 1做多
    * v
    * r
    * s
# 获取nonce
- nonceOf(address): 获取某个地址的nonce值
    * address: 输入地址


# 管理提钱
- adminClaim(address payable account,uint256 amount)          
    * account:  接收地址
    * amount:  提取金额
                            
                            
# 根据索引获取投资者信息
- getInvestor(uint256 index)   
    * index: 投资者索引
