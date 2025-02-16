# 内存の奇妙冒险 🧠——栈与堆の爱恨情仇

## 内存舞台の两位主角

### 栈（Stack）—— 单身公寓
- **住户**：原始类型（String、Number等）
- **特点**：  
  ✅ 快闪存储  
  ✅ 独立空间  
  ❌ 拒绝合租

```javascript
const savings = -5000; // 直接入住栈区
let age = 18;         // 栈区单间随时换房
```

### 堆（Heap）—— 合租大别墅
- **住户**：引用类型（Object、Array等）
- **特点**：  
  ✅ 超大空间  
  ✅ 共享地址  
  ❌ 容易串门

```javascript
const dailyLife = { // 堆区豪宅
  isSlacking: true,
  savings: -5000
};
```

---

## 变量搬家の迷惑行为大赏 🚚

### 案例1：原始类型の克隆术
```javascript
let salary = 5000;    // 栈区入住
let actualSalary = salary; // 完美克隆新房间

actualSalary = 0;     // 只修改克隆体
console.log(salary);  // 5000（原版毫发无损）
```

### 案例2：引用类型の影分身
```javascript
const slackingMethods = ['刷微博', '带薪拉屎']; // 堆区豪宅
const newMethods = slackingMethods;           // 共享门牌号

newMethods.push('假装加班'); 
console.log(slackingMethods); 
// ['刷微博', '带薪拉屎', '假装加班']（本体惨遭修改）
```

---

## 内存示意图解 🗺️

### 原始类型搬家记
```
栈区快递站 📦
----------
[ salary ] → 5000
[actualSalary] → 5000 → 0（修改后独立换房）
```

### 引用类型合租记
```
栈区门牌号 🏷️        堆区大别墅 🏠
[slackingMethods] → 🔗 → ['刷微博', '带薪拉屎']
[newMethods]     → 🔗 →     ↑ 共享同一地址
```

---

## 常见踩坑点 💣

1. **对象拷贝惨案**
```javascript
const originalObj = { skill: '摸鱼' };
const shallowCopy = originalObj; // 只是复制了地址！
shallowCopy.skill = '加班';      // 原对象也被修改
```

2. **数组传递陷阱**
```javascript
function adjustSalary(arr) {
  arr[0] = 0; // 直接修改堆区数据
}
const salaryList = [5000];
adjustSalary(salaryList); // 工资表变成[0] 😱
```

---

## 安全搬家指南 🛡️

### 深拷贝大法
```javascript
// 对象拷贝
const deepCopy = JSON.parse(JSON.stringify(originalObj));

// 数组拷贝
const newArray = [...salaryList];
```

> 下集预告：类型转换の魔术——如何把加班变成摸鱼？

💡 记住：原始类型像U盘——随身携带，引用类型像云盘——改一处处处变。内存管理就像合租——找好室友最重要！ 🏡 