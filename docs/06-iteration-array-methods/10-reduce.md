# reduce —— 归纳审判结果

`reduce` 方法可以将一个数组“归纳”成一个值，这个值可以是数字、字符串、对象……就好比把所有证据合并成一个最终判决。

## 基本用法

```javascript
const result = array.reduce((accumulator, current, index, array) => {
  // 返回新的 accumulator
}, initialValue);
```

- `accumulator`：累积器，存储上一次回调的返回值。
- `current`：当前元素。
- `initialValue`：可选，指定累积器的初始值。

### 示例：数组求和

```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((acc, num) => {
  return acc + num;
}, 0);

console.log(sum); // 15
```

### 示例：统计证据类型

```javascript
const evidenceList = [
  { type: 'fingerprint', valid: true },
  { type: 'footprint', valid: false },
  { type: 'video', valid: true }
];

const summary = evidenceList.reduce((acc, evidence) => {
  const key = evidence.valid ? 'validCount' : 'invalidCount';
  acc[key] = (acc[key] || 0) + 1;
  return acc;
}, {});

console.log(summary); // { validCount: 2, invalidCount: 1 }
```

## 注意

1. `initialValue` 很重要，尤其在处理空数组时或者想要`acc`是个对象/数组。
2. `reduce` 强大却不易读，确保用它做合适的场景。

> 下集预告：Array Method Challenges —— 结合所学数组方法，来一波终极挑战！