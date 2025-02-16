# 变量的千层套路 🍰——从青铜到王者的进化史

## 变量三兄弟：var、let、const 的爱恨情仇

### 大哥 var（退休老干部）
```javascript
var age = 18; // 随时可能被篡改
age = 28;     // 说变就变（渣男行为）
```
- **特点**：随时劈腿（可重复声明）
- **现状**：ES6后退休，建议年轻人别学

### 二哥 let（灵活单身汉）
```javascript
let savings = 0;
savings = -5000; // 灵活调整（月光族必备）
```
- **绝活**：先声明后赋值（`let girlfriend;`）
- **禁忌**：同一作用域禁止重婚（不可重复声明）

### 三弟 const（专一男）
```javascript
const PI = 3.14; 
// PI = 3.1415926  // 报错！专一男拒绝变心

const moYuManual = ['刷微博', '带薪拉屎'];
moYuManual.push('假装加班'); // 表面专一，暗地操作（数组可修改）
```
- **必杀技**：声明必须初始化（`const salary; // 报错！`）
- **隐藏技能**：对象内部属性可调教（`moYuManual.duration = '8小时'`）

---

## 变量起名的玄学 📛
### 命名潜规则
- ✅ 允许：字母、数字、_、$  
- ❌ 禁止：`let 520hongbao = ?`（数字开头达咩）  
- 🚫 禁用：`let 真的摸鱼 = '?'`（中文变量是异端！）

### 命名格式的修罗场
```javascript
// 骆驼式（主流的选择）
const slackingCoefficient = 0.87 // 老板来了记得改回0.87

// 蛇形走位（PHP遗老专用）
const slacking_coefficient = 0.87 

// 帕斯卡式（React组件专属）
const SlackingCoefficient = 0.87 // 组件大佬的尊严

// 全小写（新手村专属）
const slackingfactor = 0.87 // 读代码时：？？？
```

---

## 变量骚操作大全 🔥
### 批量生产变量
```javascript
let savings, debt, huaBei; // 三无青年套餐

const salary = 5000,
      rent = 3000,  // 打工人痛苦三连
      livingCost = 1500;
```

### 动态打补丁
```javascript
const profile = {
  name: '张三',
  workYears: '3年'
};

profile.skill = '带薪拉屎'; // 悄悄增加技能点
console.log(profile); // {name: "张三", workYears: "3年", skill: "带薪拉屎"}
```

---

## 选择困难症急救指南 🚑
1. **默认用 const** —— 专一男保平安
2. **需要劈腿用 let** —— 月光族刚需
3. **永远别用 var** —— 除非想被同事追杀

> 下集预告：数据类型的奇幻漂流——从`undefined`到`object`的奇妙冒险！

💡 记住：变量就像内裤——①每天要换（及时更新） ②别用别人的（作用域） ③别到处乱扔（全局污染） 🩲 