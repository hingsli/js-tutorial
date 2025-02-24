# 函数大法好 🧙——JS函数入门宝典

## 函数召唤术 ✨

```javascript
// 基础召唤式
function sayHello() {
  console.log('Hello World'); // 世界你好三件套
}

sayHello(); // 念动咒语 → 控制台召唤成功！
```


---

## 参数 vs 实参 🥊

### 函数菜单（参数）
```javascript
function add(num1, num2) { // 参数就像餐厅菜单
  console.log(num1 + num2); 
}
```

### 实际传参（实参）
```javascript
add(5, 10); // 实参就像点的菜 → 来份5号套餐加10号小食！
```


---

## 返回值玄学 🔄

```javascript
function subtract(num1, num2) {
  return num1 - num2; // 函数外带打包服务
  // 以下代码都是摆设（永远执行不到）
  console.log('老板说要996'); 
}

const result = subtract(10, 2); // 接过外卖小哥的包裹
console.log(result); // 8 → 真香！
```


---

## 函数生存法则 ⚡

1. **命名要风骚**：sayHello比f1更有灵魂
2. **return即退朝**：龙椅后的代码都是冷宫
3. **参数当门神**：保护函数内部变量安全
4. **多练召唤术**：函数不调用就是装饰品

> 下集剧透：作用域迷宫大冒险——全局变量 vs 局部变量的爱恨情仇

💡 记住：函数就像乐高——拼得好建大厦，拼不好...加班！ 🧱