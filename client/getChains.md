## 获取区块链列表

### 功能介绍

:::info 说明
获取支持的区块链列表
:::

### 函数原型

```go showLineNumbers
func GetChains(callback openpay_callback.Base, operationID string)
```

### 输入参数

| 参数名称    | 参数类型 | 是否必填 | 描述      |
| ----------- | -------- | -------- | --------- |
| operationID | string   | 是       | 请求 UUID |

### 返回结果

| 名称 | 类型                                           | 描述     |
| ---- | ---------------------------------------------- | -------- |
| ~    | List<[ChainInfo](/common/entity.md#chaininfo)> | 链列表   |

### 代码示例

```go showLineNumbers
 SDK.GetChains(ParamsUtil.buildOperationID())
```