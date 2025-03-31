# 真假莫辨 —— JavaScript中的 Truthy 与 Falsy

在法庭上，“证据有效”与“证据无效”是关键信息。在JavaScript中，同样有“真值”（truthy）和“假值”（falsy）的概念。当我们把一个值放到条件判断里时，它会被隐式转换为布尔值，这就需要我们清楚哪些值是真、哪些为假。

## Falsy 值有哪些？ 🕵️
- `false`
- `0`（数字零）
- `''`或`""`（空字符串）
- `null`
- `undefined`
- `NaN`

只要是这六类值，在条件判断中会被当作`false`处理。

### 例子
```javascript
if (0) {
  console.log('这行不会被执行');
} else {
  console.log('0在条件中是false');
}

if ('') {
  console.log('空字符串也是false');
} else {
  console.log('空字符串在条件中是false');
}
```

## Truthy 值 📈
除上述六种“falsy”外的其他值，都是“truthy”。包括`[]`（空数组）、`{}`（空对象）、任意非空字符串等。

```javascript
if ([]) {
  console.log('空数组是truthy！');
}
if ('false') {
  console.log('非空字符串是truthy！');
}
```

## 常见陷阱 ⚠️
1. **`==` vs `===`**：用`==`时，`0 == false`会是`true`，容易产生歧义。  
2. **隐式转换**：`if (someArray) {}` 仅仅判断数组是否“存在”，不意味着数组里一定有数据。

> 下集预告：逻辑运算符——AND、OR、NOT大比拼！  