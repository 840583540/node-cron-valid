# node-cron-valid 描述
   1. 基于 [node-cron](https://github.com/kelektiv/node-cron)，实现 corn 输入验证，中文提示，
   2. 用途：主要用于手动输入 corn 表达式，验证输入是否符合 cron 规范
## 说明
   ### 验证顺序 
   秒-分-小时-周-天-月      （-代表空格）
   ### 验证范围
   - 秒  0-59
   - 分  0-59
 - 小时  0-23
 - 星期  0-6 （0代表星期天，允许输入英文简写）
 - 天  1-31
 - 月  1-12
## 调用方法
```javascript
// 1. 引入node-cron-vaild.js
   const cron = require('@/plugins/node-cron-valid/node-cron-vaild.js')
// 2. 调用验证方法
   const result = cron.validate(value,config)
   value // 需要验证的表达式 string

   config // 基础配置 Object
   config.language = en // 英文提示， 默认
   config.language = ch // 中文提示

   @return result.status // 表达式验证是否通过
   @return result.msg // 验证失败提示语
```
