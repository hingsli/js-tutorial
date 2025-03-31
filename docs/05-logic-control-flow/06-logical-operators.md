# 三剑客齐聚 —— 逻辑运算符 AND、OR、NOT

法庭上，证据需要合并、排除或取反；在JavaScript中，我们也有三把利剑：`&&`（与）、`||`（或）、`!`（非）。它们能帮我们构建更复杂的逻辑判断。

## 逻辑与（&&）🗡️
只有当“左右手”都为真时，结果才为真，否则为假。

```javascript
const hasEvidenceA = true;
const hasEvidenceB = false;

if (hasEvidenceA && hasEvidenceB) {
  console.log('两份证据都确凿，罪名成立！');
} else {
  console.log('证据不够充分，继续调查。');
}
```

> 逻辑与在遇到`falsy`值时会直接返回该`falsy`值。

## 逻辑或（||）🛡️
只要“左右手”有一方为真，结果就为真，否则为假。

```javascript
const confession = false;
const witnessTestimony = true;

if (confession || witnessTestimony) {
  console.log('任何一个证据成立，都能定罪！');
} else {
  console.log('缺乏关键证据，无法定罪。');
}
```

> 逻辑或在遇到`truthy`值时会返回该`truthy`值。

## 逻辑非（!）🔄
用来取反，`!true === false`，`!false === true`。

```javascript
const isGuilty = true;

if (!isGuilty) {
  console.log('被告清白！');
} else {
  console.log('被告有罪！');
}
```

> 下集预告：逻辑赋值运算符——赋值新招式，一举多得！  