## 获取交易执行所需 Gas

### 功能介绍

:::info 说明
根据交易数据获取不同速率的 gas 集合, 用于转账前 gas 费率确认
:::

### 函数原型

```go showLineNumbers
func GetEstimatedGas(callback openpay_callback.Base, operationID string, transferInfo string)
```

### 输入参数

| 参数名称     | 参数类型 | 是否必填 | 描述                                       |
| ------------ | -------- | -------- | ------------------------------------------ |
| operationID  | string   | 是       | 请求 UUID                                  |
| transferInfo | Object   | 是       | [交易对象](/common/entity.md#transferinfo) |

### 返回结果

| 名称 | 类型                                 | 描述     |
| ---- | ------------------------------------ | -------- |
| ~    | [GasInfo](/common/entity.md#gasinfo) | gas 信息 |

### 代码示例

```go showLineNumbers
 SDK.GetEstimatedGas(ParamsUtil.buildOperationID(), "")
```