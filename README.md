# node-cron-valid
基于 [node-cron](https://github.com/kelektiv/node-cron)，实现 corn 输入验证，中文提示

### 调用方法
```javascript
 // 1. 引入node-cron-vaild.js
const cron = require('@/plugins/node-cron-valid/node-cron-vaild.js')

const result = cron.validate(value,config)
value // 需要验证的表达式 string

config // 基础配置 Object
config.language = en // 英文提示， 默认
config.language = ch // 中文提示

@return result.status // 表达式验证是否通过
@return result.msg // 验证失败提示语
```
