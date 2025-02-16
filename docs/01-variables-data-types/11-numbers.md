# 数字の变形记 🔢——JS数字操作完全指南

## 数字包装术 💰

```javascript
const salary = new Number(996); // 把数字包装成土豪金对象
console.log(typeof salary); // "object" → 现在是个尊贵的对象了
```

---

## 常用方法大全 🧰

### 1. 变装字符串
```javascript
// 基础变身
console.log(salary.toString()); // '996' → 现在是个字符串打工人

// 查看数字长度（摸鱼技巧）
console.log(salary.toString().length); // 3 → 三位数工资
```

### 2. 假装有零钱
```javascript
const bonus = 3.1415;
console.log(bonus.toFixed(2)); // '3.14' → 财务说四舍五入
```

### 3. 有效数字秀
```javascript
const pi = 3.1415926;
console.log(pi.toPrecision(3)); // '3.14' → 只保留三位有效数字
```

### 4. 科学记数法
```javascript
const annualSalary = 1000000;
console.log(annualSalary.toExponential(2)); // '1.00e+6' → 百万年薪的体面写法
```

### 5. 摸鱼式转换
```javascript
const income = 1234567.89;
console.log(income.toLocaleString('zh-CN')); // '1,234,567.89' → 国际范数字
```

---

## 极值探索 🚀

```javascript
// 最大安全数（老板的工资上限）
console.log(Number.MAX_VALUE); // 1.7976931348623157e+308

// 最小安全数（实习生的工资）
console.log(Number.MIN_VALUE); // 5e-324
```

---

## 生存法则 ⚔️

1. **慎用Number对象**：直接写数字更高效（`5` vs `new Number(5)`）
2. **财务计算用toFixed**：但要注意四舍五入的坑
3. **大数用科学记数法**：防止数字溢出变成`Infinity`
4. **本地化显示金额**：`toLocaleString`让数字更友好

> 下集预告：Math对象の魔法——从圆周率到随机数的奇妙之旅

💡 记住：数字就像水——用对了载舟，用错了...加班！ 💦 