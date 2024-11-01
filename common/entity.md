## WalletConfig

> SDK 初始化配置

| 字段名                                    | 类型   | 说明                   |
| ----------------------------------------- | ------ | ---------------------- |
| api_addr                                  | string | 服务端 api 地址        |
| ws_addr                                   | string | 服务端 ws 地址         |
| [platform_id](/common/enum.md#platformid) | int32  | 平台 ID                |
| data_dir                                  | string | 数据目录               |
| [log_level](/common/enum.md#loglevel)    | uint32 | 日志级别               |
| is_log_standard_output                    | bool   | 是否日志输出到标准输出 |
| log_file_path                             | string | 日志文件路径           |

## KeyInfo

> 链 key 信息

| 字段名      | 类型   | 说明         |
| ----------- | ------ | ------------ |
| wallet_type | int    | 钱包类型     |
| address     | string | 地址         |
| mnemonic    | string | 助记词       |
| private_key | string | hex 编码私钥 |

## ChainInfo

> 区块链信息

| 字段名       | 类型   | 说明                                |
| ------------ | ------ | ----------------------------------- |
| name         | string | 链名称                              |
| wallet_type  | string | [链类型](/common/enum.md#chaintype) |
| icon         | string | icon                                |
| total_assets | string | 总资产                              |

## TokenInfo

> Token 信息

| 字段名            | 类型   | 说明                                |
| ----------------- | ------ | ----------------------------------- |
| wallet_type       | string | [链类型](/common/enum.md#chaintype) |
| name              | string | 名称                                |
| symbol            | string | 符号                                |
| icon              | string | 图标                                |
| decimals          | int    | 精度                                |
| balance           | string | 余额                                |
| is_multiple_chain | bool   | 是否是多链代币                      |
| usdt_balance      | string | USDT 余额                           |

## TransferInfo

> 发起交易信息

| 字段名       | 类型   | 是否必填 | 说明         |
| ------------ | ------ | -------- | ------------ |
| from_address | string | 是       | 发送钱包地址 |
| to_address   | string | 是       | 接收钱包地址 |
| gas          | string | 否       | Gas 数量     |
| gas_limit    | string | 否       | Gas 上限     |
| amount       | string | 是       | 金额         |
| wallet_type  | int    | 是       | 钱包类型     |
| token_name   | string | 是       | 代币名称     |

## TransactionInfo

> 交易信息

| 字段名              | 类型   | 说明                                   |
| ------------------- | ------ | -------------------------------------- |
| transaction_hash    | string | 交易哈希                               |
| transaction_index   | int    | 交易索引                               |
| block_number        | int    | 区块号                                 |
| block_hash          | string | 区块哈希                               |
| from_address        | string | 发送钱包地址                           |
| to_address          | string | 接收钱包地址                           |
| amount              | string | 金额                                   |
| gas_used            | int    | Gas 使用量                             |
| gas_price           | string | Gas 价格                               |
| cumulative_gas_used | int    | 累计 Gas 使用量                        |
| status              | int    | 状态 -1:转账中, 0:转账失败, 1:转账成功 |
| token_name          | string | 代币名称                               |
| contract_address    | string | 合约地址                               |
| wallet_type         | int    | [链类型](/common/enum.md#chiantype)    |
| transaction_type    | int    | 交易类型 1:转入 2:转出                 |
| create_time         | int    | 交易时间                               |

## GasInfo

> GasInfo

| 字段名  | 类型   | 说明   |
| ------- | ------ | ------ |
| gas     | string | Gas    |
| gas_fee | string | Gas 费 |

## AddressValidateInfo

| 字段名  | 类型     | 说明                   |
| ------- | -------- | ---------------------- |
| address | string   | 钱包地址               |
| matched | bool     | 是否匹配               |
| chains  | []string | 符合地址规范的链名数组 |