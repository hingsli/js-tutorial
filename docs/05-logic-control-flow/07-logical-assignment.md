# 逻辑赋值运算符 —— 省时省力的判决书

ES2021 引入了三个新的逻辑赋值运算符，让你在做逻辑判断的同时直接给变量赋值，简化了不少写法。

## 运算符概览 📝
1. `x ||= y` —— 如果 `x` 是 falsy，则 `x = y`
2. `x &&= y` —— 如果 `x` 是 truthy，则 `x = y`
3. `x ??= y` —— 如果 `x` 为 `null` 或 `undefined`，则 `x = y`

### OR 赋值（||=）
```javascript
let sentence = '';
sentence ||= '暂未填写陈述';
// 因为 sentence 是空字符串(falsy)，所以会赋值
console.log(sentence); // '暂未填写陈述'
```

### AND 赋值（&&=）
```javascript
let judgeName = '包青天';
judgeName &&= '宋慈';
// judgeName是truthy，所以judgeName被替换
console.log(judgeName); // '宋慈'
```

### Nullish 赋值（??=）
```javascript
let defendant;
defendant ??= '无名氏';
// 只有当 defendant 是 null 或 undefined 时才会被赋值
console.log(defendant); // '无名氏'

let witness = '';
witness ??= '老王';
console.log(witness); // '' (因为空字符串不属于 null/undefined)
```

## 适用场景 💡
- 设置默认值时，使用 `||=` 或 `??=`  
- 在确保存在某变量后再替换时，用 `&&=`  
- 让代码更短、更易读，但要小心区分“falsy”与“null/undefined”的差异。

> 下集预告：三元运算符——写法优雅的简易判决！  