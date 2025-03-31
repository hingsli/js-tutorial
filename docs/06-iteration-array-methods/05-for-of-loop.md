# 审阅者的福音 —— for...of 循环

当我们需要遍历数组或其他可迭代对象时，`for...of` 为我们提供了一种简洁且可读性高的方式。就像法官翻阅一个证据清单，无需关心索引，只关心条目内容。

## 基础用法

```javascript
const evidenceList = ['指纹', '脚印', '录像', '证人证言'];

for (const evidence of evidenceList) {
  console.log('证据：', evidence);
}
```
- 与传统的 `for (let i = 0; i < arr.length; i++)` 相比，不需要手动处理索引。
- 适用于数组、字符串、Map、Set 等等——只要对象可迭代。

## 字符串也能遍历

```javascript
const suspectName = 'ZhangSan';
for (const char of suspectName) {
  console.log('名字中的字符：', char);
}
```

## 注意事项

- `for...of` 得到的是**值**，并不直接提供索引。如果你需要索引，可能要借助 `entries()` 或传统 `for` 循环。

> 下集预告：`for...in` 循环——对象属性的勘察官！