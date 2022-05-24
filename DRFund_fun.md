
## DRFund_contract

dev endpoint: `http://18.180.227.173:8545/`

### DRStock `0x73C696a4FdDeA2177b6b21aC4cbff879DF7B576c`

**Function**
      
## 用户取钱
- claim(address account, uint256 amount, uint256 nonce, string memory stockCode, uint256 index, uint8 v, bytes32 r, bytes32 s) 
  * account:用户地址
  * amount: 金额
  * nonce：nonce
  * stockCode：股票代码
  * index：投资股票索引
  * v: v
  * r: r
  * s: s

## 管理员取钱
- ownerClaim(address account, uint256 amount)
  * account：接收者地址
  * amount:提取金额

## 获取nonce值
- nonceOf(address): 获取某个地址的nonce值
    * address: 输入地址

**Event**

```solidity
event Claim(address from, address to, uint256 amount, uint256 nonce, string stockCode, uint256 index, uint256 timestamp);
event OwnerClaim(address from, address to, uint256 amount, uint256 timestamp);
```
