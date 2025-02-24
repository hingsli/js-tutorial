# 参数七十二变 🎭——JS函数传参秘籍

## 备胎参数养成记 🤖

```javascript
// 旧时代的手动挡
function registerUser(user) {
  if (!user) {
    user = 'Bot'; // 手动设置备胎
  }
}

// 新时代的自动挡
function registerVIP(user = 'SVIP') { // 默认参数像备胎随时待命
  return `${user} 已成功充值信仰！`;
}
console.log(registerVIP()); // SVIP 已成功充值信仰！
```


---

## 吃货参数(...) 🍔

```javascript
function sum(...numbers) { // 三个点开启吃货模式
  let total = 0;
  for (const num of numbers) {
    total += num; // 吃货的胃容量无上限
  }
  return total;
}
console.log(sum(1, 2, 3, 4, 5)); // 15 → 轻松消化！
```


---

## 对象参数拆快递 📦

```javascript
function loginUser({ id, name }) { // 对象拆箱就像拆快递
  return `用户 ${name} (ID:${id}) 已登录！`;
}

const user = { id: 666, name: '码神' };
console.log(loginUser(user)); // 用户 码神 (ID:666) 已登录！
```


---

## 数组参数抽奖系统 🎰

```javascript
function randomDraw(prizes) {
  const riggedIndex = Math.floor(Math.random() * prizes.length); // 老板说要有黑幕
  return prizes[riggedIndex]; 
}

console.log(randomDraw(['谢谢参与', '再来一次', 'PS5', '老板内定'])); // 你猜中了啥？
```


---

## 参数生存指南 🧭

1. **默认参数是备胎**：永远做好最坏打算
2. **...操作符像吃货**：有多少参数吃多少
3. **对象参数要拆箱**：像拆快递一样爽快
4. **数组参数会抽奖**：小心老板内定大奖
5. **参数命名要规范**：英文变量+中文注释最佳实践

> 下集预告：作用域迷宫大冒险——全局变量与局部变量的爱恨情仇

💡 记住：参数就像调味料——放对了是美味，放错了...加班！ 🧂