# 函数大挑战 💻🔥

学完函数基本功，来试试这些骚操作！

## 挑战1：温度转换侠 🌡️

**任务说明：**
创建一个叫`getCelsius()`的函数，把华氏度变成摄氏度。如果能用一行箭头函数搞定，老板给你加鸡腿 🍗

**效果预览：**
```JavaScript
console.log(getCelsius(32)); // 0
console.log(`体温 ${getCelsius(98.6)}°C 正常`); // 体温 37°C 正常
```

**祖传配方：**
`(F - 32) * 5 / 9` → [配方来源](https://www.cuemath.com/fahrenheit-to-celsius-formula/)

<details>
  <summary>参考答案</summary>
  
```JavaScript
// 摸鱼式简写
const getCelsius = f => Math.round((f - 32) * 5 / 9);
console.log(`体温 ${getCelsius(98.6)}°C 正常`); // 深藏功与名
```
</details>

## 挑战2：数组侦探 🔍

**任务说明：**
用箭头函数`minMax()`找出数组中的最小值和最大值，返回一个对象（社畜的基本操作）

**效果预览：**
```JavaScript
console.log(minMax([1, 2, 3, 4, 5])); // { min: 1, max: 5 }
```

**破案线索：**
1. `Math.min/max` + 三点运算符 → 数组克星
2. 对象简写语法 → 少打字多摸鱼

<details>
  <summary>参考答案</summary>
  
```JavaScript
const minMax = arr => ({ 
  min: Math.min(...arr), 
  max: Math.max(...arr) 
});
// 社畜快乐码：用最短的代码，加最晚的班
```
</details>

## 挑战3：社畜的觉悟 🚀

**任务说明：**
创建立即执行函数(IIFE)，页面加载时自动计算矩形面积并输出（深藏功与名的艺术）

**效果预览：**
```JavaScript
// 页面加载时自动触发
"长10宽5的矩形面积是50"
```

**生存指南：**
1. 面积公式：长 × 宽 → 打工人的数学
2. 直接console.log → 事了拂衣去

<details>
  <summary>参考答案</summary>
  
```JavaScript
((长, 宽) => console.log(`长${长}宽${宽}的矩形面积是${长*宽}`))(10, 5);
// 立即执行函数的奥义：写完就跑真刺激
```
</details>
