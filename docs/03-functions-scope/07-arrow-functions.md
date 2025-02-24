# 箭头函数的逆袭 🏹——打工人的华丽变身

## 基础变身术 🦸♂️

```javascript
// 传统打工人
function add(a, b) {
  return a + b;
}

// 箭头函数版
const add = (a, b) => {
  return a + b;
};
console.log(add(1, 2)); // 3 → 功能不变，造型更酷
```

---

## 社畜式简写 📉

### 隐式返回（老板最爱）
```javascript
const subtract = (a, b) => a - b; // 连return都省了！
console.log(subtract(10, 5)); // 5
```

### 单身参数特权
```javascript
const double = a => a * 2; // 单身狗专属括号豁免权
console.log(double(10)); // 20
```

### 对象返回的艺术
```javascript
const createObj = () => ({ name: 'Brad' }); // 用括号守护对象尊严
console.log(createObj()); // {name: 'Brad'}
```

---

## 回调函数的春天 🌸

```javascript
const numbers = [1, 2, 3, 4, 5];

// 传统回调写法
numbers.forEach(function(n) {
  console.log(n); // 1 2 3 4 5
});

// 箭头函数优雅版
numbers.forEach(n => console.log(n)); // 1 2 3 4 5
```

---

## 箭头函数生存指南 🧭

1. **=> 是时尚单品**：比function更简洁有型
2. **隐式返回是摸鱼**：能省则省（单行表达式限定）
3. **单身参数特权**：可以不要括号（但多参数不行）
4. **对象返回要包装**：用()保护你的对象
5. **回调函数好搭档**：让代码更风骚

> 下集预告：立即执行函数——代码界的快闪族 🚀

💡 记住：箭头函数就像表情包——用对了让代码更生动！ 🎭