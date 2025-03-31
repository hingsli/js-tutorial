# map —— 证据加工厂

当我们想批量修改或加工数组的每个元素时，可以使用 `map` 方法，就像开设了一条流水线，为证据依次贴上新的标签，生成一个新的证据数组。

## 基本用法

```javascript
const newArray = array.map((element, index, array) => {
  // 返回一个新的值，组成新的数组
});
```

### 示例

```javascript
const evidenceList = [
  { type: 'fingerprint', valid: true },
  { type: 'footprint', valid: false },
  { type: 'video', valid: true }
];

// 为每个证据添加标识文本
const processedEvidence = evidenceList.map(evidence => {
  return {
    ...evidence,
    label: evidence.valid ? '有效证据' : '无效证据'
  };
});

console.log(processedEvidence);
// [
//   { type: 'fingerprint', valid: true, label: '有效证据' },
//   { type: 'footprint', valid: false, label: '无效证据' },
//   { type: 'video', valid: true, label: '有效证据' }
// ]
```

## 注意

1. **不会修改原数组**，返回的数组长度与原数组相同。
2. 回调函数返回的值会成为新数组的元素。

> 下集预告：reduce —— 如何将证据整体归纳成一个最终结论？