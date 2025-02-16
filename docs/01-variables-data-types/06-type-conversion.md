# 类型转换的魔术秀 🎩——JS的72变秘籍

## 基本类型转换三连

### 1. 字符串 → 数字（点石成金）
```javascript
let amount = '100'; // 初始是字符串

// 方法1：parseInt大法（整数专用）
amount = parseInt(amount); // 100 → number

// 方法2：一元加号（最潮姿势）
amount = +amount;         // 100 → number 

// 方法3：Number构造函数（老干部风）
amount = Number(amount);  // 100 → number
```

### 2. 数字 → 字符串（化功大法）
```javascript
amount = 100; // 先变回数字

// 方法1：toString召唤术
amount = amount.toString(); // '100' → string

// 方法2：String点化术 
amount = String(amount);    // '100' → string
```

### 3. 浮点数的优雅转换
```javascript
let price = '99.5元';

// parseInt会截肢 → 99（血亏0.5）
// parseFloat保全身 → 99.5
price = parseFloat(price); // 99.5 → number
```

---

## 高级骚操作 💫

### 布尔值的真假美猴王
```javascript
let salary = 1;

// 非零数字 → true（打工人的希望）
salary = Boolean(salary); // true → boolean

let balance = 0;
// 零 → false（钱包的真实）
balance = Boolean(balance); // false → boolean
```

---

## NaN迷惑行为大赏 🤡

### 五种召唤NaN的邪术
```javascript
// 1. 数学老师的噩梦
console.log(Math.sqrt(-1)); // √-1 → NaN 

// 2. 量子叠加态计算
console.log(1 + NaN);       // NaN 

// 3. 薛定谔的undefined
console.log(undefined + undefined); // NaN

// 4. 字符串的阴谋
console.log('摸鱼' / 3);    // NaN

// 5. 强扭的瓜不甜
let amount = 'hello';
console.log(Number(amount)); // NaN
```

---

## 类型转换的生存法则 ⚔️

1. **表单数据必转换**：`<input>`来的都是字符串
2. **浮点请用parseFloat**：避免parseInt的截肢惨案
3. **零值判断要小心**：`0 == false` → true（JS的陷阱）

> 下集预告：运算符的奇妙冒险——+号竟能连接世界？

💡 记住：类型转换就像化妆——适度的修饰（显式转换）更美丽，过度的自动（隐式转换）易翻车！ 💄 