# forEach —— 用回调函数审阅数组

在遍历数组时，除了循环语句，还有一种更“函数式”的写法，就是使用数组的 `forEach` 方法。它可以将逻辑封装到回调函数中，让代码更简洁。

## 基本语法

```javascript
array.forEach((element, index, array) => {
  // 对每个元素执行的操作
});
```

- `element`：当前遍历到的元素
- `index`：该元素的索引
- `array`：整个数组本身

### 示例

```javascript
const jurors = ['Alice', 'Bob', 'Charlie'];

jurors.forEach((juror, idx) => {
  console.log(`陪审员 #${idx}: ${juror}`);
});
```

## 特点

1. **不能中途 break**：`forEach` 并没有内置 `break` 或 `continue` 的机制，想要提前结束，需要其它方法（比如抛异常）。
2. **回调函数**：能避免手动维护计数器或索引变量。

> 下集预告：filter —— 筛选证据，用于过滤数组中的特定元素！