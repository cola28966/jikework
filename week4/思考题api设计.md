# 01 思考题

## 1.1 api
名称 authByUserNameAndPassword
类型 POST

## 1.2 参数

### 1.2.1 入参 
authByUserNameAndPasswordReq


| 参数名称 |  描述 |类型 | 是否必传 |
| --- | --- | --- |--- |
| userName | 用户名 |string | 是 |
| password | 密码 |string | 是 |
| loginIp | ⽤户IP |string | 否 |
| deviceId | 设备号 |string | 否 |
| deviceType | 设备类型 |int | 否 |

### 1.2.2 返回结果


authByUserNameAndPasswordRep

| 参数名称 | 描述 | 类型 | 是否必传 |
| --- | --- | --- | --- |
| code | 状态码 200 成功 | int | 是 |
| msg | 返回信息 | string | 否 |
| data | 返回数据 | authData | 是 |

authData
| 参数名称 | 描述 | 类型 | 是否必传 |
| --- | --- | --- | --- |
| access_token | 返回信息 | string | 是 |
| refresh_token | 返回信息 | string | 是 |
| expireTimeMillis| 过期时间 | string | 是 |
| userId | 用户id | Long | 是 |

