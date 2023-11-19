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
| accessToken | 短 token | string | 是 |
| refreshToken | 长 token | string | 是 |
| expireTimeMillis| 过期时间 | string | 是 |
| userId | 用户id | Long | 是 |

# 02 思考

1. 参数命名要通俗易懂，长短 token 的字段命名，一开始是想不到命名accessToken 和 refreshToken 这两个字段的，在谷歌了认证中的长短 token 后，使用到了这两个词，也和课程中的一致，命名可以参考常规解决方案中别人的命名
2. 考虑要全面，一开始设计接口的入参，是没有想到风控相关的，后面对比课程中设计后，补上的
3. 入参和出参都只使用一个对象
