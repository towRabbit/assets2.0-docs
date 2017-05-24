# 过滤器

过滤器是一个通过输入数据，能够及时对数据进行处理并返回一个数据结果的简单函数。

## 用法
过滤器通常会使用管道标志 “ | ”， 比如：
```vue
{{ msg | uppercase  }}
// 'abc' => 'ABC'
```
### 嵌套使用
```vue
{{ msg | uppercase | tonumber }}
```
### 带参数的过滤器
```vue
{{ msg | uppercase(agr1, agr2,...) }}
```

## defData

>对数据进行过滤，如果数据为`null`显示`—`

可带参数，数据单位，例如：

```html
<div>{{ count | defData('元') }}</div>
<script>
  new Vue({
    el: '#main',
    data: { count: 1000 }
  })
</script>

// 1000元
```

## moneyFlat

>对金额数据格式化

```html
<div>{{ 1000 | moneyFlat }}</div>

// 格式化 -> 1,000.00
```

## busRate

>通过__企业评级__编号得到对应字段


key | value
---|---
0 | 最低风险
1 | 人工审核
2 | 拒绝申请
3 | 黑名单

!> fliter 用于过滤展示数据，不可用于下拉框数据使用

## busType

>通过__企业注册类型__编号得到对应字段

## busInfo
>通过__行业信息__（包括行业大类，集齐细分）编号得到对应字段

## busRole
>通过__企业角色__编号得到对应字段