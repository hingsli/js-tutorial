# 块作用域王国 🏰——变量们的临时帐篷

## 块级作用域生存法则 ⛺

```javascript
const x = 100; // 全局公告牌

if (true) {
  const y = 200; // if 块里的临时帐篷
  console.log(x + y); // 300 → 可以看全局公告
}

// console.log(y); ❌ 报错！帐篷拆了别想找
```

---

## 循环变量监狱 🔄

```javascript
for (let i = 0; i <= 10; i++) { // let 是遵纪守法的好公民
  console.log(i); // 乖乖待在循环监狱里
}

// console.log(i); ❌ 报错！刑满释放别想找
```

---

## var 的越狱技巧 🦹

```javascript
if (true) {
  var c = 700; // var 是块作用域的钉子户
}
console.log(c); // 700 → 成功越狱！

function run() {
  var d = 100; // 函数是 var 的终极监狱
}
run();
// console.log(d); ❌ 报错！这次越狱失败
```

---

## 全局变量绑架案 🕵️

```javascript
const foo = 1; // 良民不上交 window
var bar = 2;    // var 主动投靠 window 帮派

console.log(window.bar); // 2 → 黑帮成员登记在册
console.log(window.foo); // undefined → 良民清清白白
```

---

## 变量生存指南 🧭

1. **let/const 是模范公民**：乖乖待在块级帐篷里
2. **var 是越狱惯犯**：除了函数监狱哪都关不住
3. **循环变量要坐牢**：出循环就别想找到
4. **全局声明要谨慎**：var 会主动投靠 window 帮派

