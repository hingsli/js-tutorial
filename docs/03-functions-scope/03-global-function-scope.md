# 作用域江湖 🌐——变量们的生存法则

## 全局大佬 Window 👑

```javascript
// 武林盟主 window 统领全局
console.log(window.innerWidth); // 浏览器江湖的宽度
alert('有内鬼！'); // window 的独门绝技
```

---

## 全局变量 vs 函数变量 🥊

### 全局变量（公共场所）
```javascript
const x = 100; // 全江湖可见的公告牌

function checkNotice() {
  console.log(x); // 100 → 走到哪都能看见
}
checkNotice();

if (true) {
  console.log(x); // 100 → 厕所里也能瞅见
}
```

### 函数变量（私人领地）
```javascript
function secretRoom() {
  const y = 50; // 函数内部的私房钱
  console.log(y); // 50 → 自家保险箱随便看
}
secretRoom();

console.log(y); // ❌ 报错！别人家的保险箱可看不得
```

---

## 变量套娃术 🪆

```javascript
const x = 100; // 全局大佬

function shadowClone() {
  const x = 1; // 局部影分身
  const y = 50;
  console.log(x + y); // 51 → 优先使用自己的分身
}

shadowClone();
console.log(x); // 100 → 本体安然无恙
```

---

## 作用域生存指南 🧭

1. **全局变量像广场舞**：谁都能来踩一脚（慎用！）
2. **函数变量像保险箱**：自家钥匙自家管
3. **变量套娃要谨慎**：容易搞不清本体和分身
4. **window 是江湖百晓生**：啥都知道但别乱用

> 下集预告：块作用域登场——if/for 语句里的临时帐篷 🏕️

💡 记住：作用域就像厕所隔间——进错门会很尴尬！ 🚽
