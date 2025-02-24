# 立即执行函数快闪族 🚀——代码界的瞬间艺术

## 匿名函数自爆术 💥

```javascript:08-iife/script.js
// 基本款快闪（创建即运行）
(function() {
  const user = 'John'; // 安全屋里的变量
  console.log(user); // John → 不会污染全局
  
  const hello = () => console.log('来自IIFE的问候');
  hello(); // 安全屋内部呼叫
})();
```

---

## 传参版快闪 🎁

```javascript:08-iife/script.js
// 快闪时传递秘密情报
(function(name) {
  console.log('Hello ' + name); // 接头暗号
})('Shawn'); // 立即传递参数
```

---

## 危险动作请勿模仿 ☠️

```javascript:08-iife/script.js
// 命名IIFE（递归自杀式快闪）
(function hello() {
  console.log('Hello');
  hello(); // 无限自嗨 → 浏览器崩溃警告！
})();
```

---

## 全局污染大作战 🛡️

```javascript:08-iife/otherscript.js
// 其他脚本的全局炸弹 💣
const user = 'Brad';
console.log(user); // Brad → 全局污染源
```

```javascript:08-iife/script.js
// IIFE隔离舱 🚧
(function() {
  const user = 'John'; // 安全隔离
  console.log(user); // John → 与Brad和平共处
})();
```

---

## IIFE生存指南 🧭

1. **快闪原则**：创建即运行，深藏功与名
2. **匿名是美德**：用完即焚不留痕
3. **参数像暗号**：传递后立即销毁
4. **隔离舱万岁**：保护全局变量安全
5. **命名需谨慎**：除非想玩递归俄罗斯轮盘

> 下集预告：函数挑战赛——代码奥林匹克的入场券 🏅

💡 记住：IIFE就像特工——完成任务后不留痕迹！ 🕶️