# BitcoinSV - BSV

### 文档版本：1.0.3
检查日期: 2020.05.10

### 官网地址：
https://bitcoinsv.io/

### 钱包下载：
https://download.bitcoinsv.io/bitcoinsv/

### 查询网站：
https://bsv.btc.com/

### 开发文档
* 同 BTC - Bitcoin

### 安装说明：
* 同 BTC - Bitcoin

### 配置文件：
* 同 BTC - Bitcoin

### 升级说明：
* 同 BTC - Bitcoin

### 创建地址：
* 同 BTC - Bitcoin

### 追踪入账：
* 同 BTC - Bitcoin

### 对外提币：
1、估算当前费用
```
estimatefee 接口已取消，官方文档说默认的fee是: 0.5sat/byte，根据这个计算预留的fee就行了。
```

2、创建RAW交易
```
curl -X POST -H 'content-type: text/plain;' http://127.0.0.1:8332/ -u RPC用户:RPC密码 \
-d '{"jsonrpc":"1.0","id":"随便写","method":"createrawtransaction","params":[[{"txid":"输出的Txid","vout":输出的Tx的序号}],[{"接收地址":接收金额}]}'  
```

3、导入私钥（如果私钥已在节点上，可跳过）
```
curl -X POST -H 'content-type: text/plain;' http://127.0.0.1:8332/ -u RPC用户:RPC密码 \
-d '{"jsonrpc":"1.0","id":"随便写","method":"importprivkey","params":["私钥密文","标签（可留空）",false]}'  
```

4、签名RAW交易
```
curl -X POST -H 'content-type: text/plain;' http://127.0.0.1:8332/ -u RPC用户:RPC密码 \
-d '{"jsonrpc":"1.0","id":"随便写","method":"signrawtransaction","params":["创建RAW返回的Hex"]}'  
```

5、发送RAW交易
```
curl -X POST -H 'content-type: text/plain;' http://127.0.0.1:8332/ -u RPC用户:RPC密码 \
-d '{"jsonrpc":"1.0","id":"随便写","method":"sendrawtransaction","params":["完成签名的Hex"]}'  
```

### 归集处理：
* 同 BTC - Bitcoin

### 灾难恢复：
* 同 BTC - Bitcoin

### 注意事项：
