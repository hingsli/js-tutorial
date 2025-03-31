# 对象属性勘察官 —— for...in 循环

如果你想要遍历对象的可枚举属性，`for...in` 就是你的好帮手。它就像一名勘察官，会挨个查看对象的“可见”属性。

## 基础用法

```javascript
const suspect = {
  name: 'LiSi',
  age: 28,
  crimeLevel: 'medium'
};

for (const key in suspect) {
  console.log('属性名:', key, '属性值:', suspect[key]);
}
```
- `key` 是属性名，也可以用 `suspect[key]` 访问对应值。

## 与 for...of 的区别

- `for...in`：专注对象**可枚举属性**的遍历，但也可用在数组上（会遍历数组索引）。
- `for...of`：专注**可迭代对象**的遍历，直接获得值，而非索引或属性名。

## 小心坑点

1. **原型链上的属性**：`for...in` 也会遍历到对象原型链上的可枚举属性。  
2. **数组遍历**：用 `for...in` 遍历数组不算最佳实践，可能出现意想不到的顺序。

> 下集预告：`forEach` 回调——数组遍历的新姿势！