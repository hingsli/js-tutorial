# filter —— 证据筛选专家

在审案过程中，我们常需要从庞大的证据集中筛选出有价值的部分。数组的 `filter` 方法，就能帮助你过滤出符合条件的元素，生成新数组。

## 基本用法

```javascript
const newArray = array.filter((element, index, array) => {
  // 返回一个布尔值
  // true 表示保留该元素，false 表示舍弃
});
```

### 示例

```javascript
const evidenceList = [
  { type: 'fingerprint', valid: true },
  { type: 'footprint', valid: false },
  { type: 'video', valid: true }
];

const validEvidence = evidenceList.filter(evidence => evidence.valid);

console.log(validEvidence);
// [
//   { type: 'fingerprint', valid: true },
//   { type: 'video', valid: true }
// ]
```

## 注意

1. **不会修改原数组**，而是返回一个新数组。
2. 条件必须返回布尔值，`true` 表示元素通过过滤。

> 下集预告：map —— 将证据转换或加工处理，生成全新结果！