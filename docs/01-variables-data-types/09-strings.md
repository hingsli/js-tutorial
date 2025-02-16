# 字符串の七十二变 🎭——从青铜到铂金的骚操作大全

## 基础招式篇

### 1. 传统拼接 vs 魔法拼接
```javascript
const name = 'John';
const age = 31;

// 传统拼接（老古董写法）
let greeting = 'Hello, my name is ' + name + ' and I am ' + age + ' years old';

// 模板字面量（现代魔法）
greeting = `Hello, my name is ${name} and I am ${age} years old`;
```

### 2. 字符串对象の诞生
```javascript
const slogan = new String('摸鱼是人类进步的阶梯');
console.log(typeof slogan); // "object" → 包装成土豪对象
```

---

## 属性技能树 🌳

### 1. 长度检测
```javascript
const motto = '带薪拉屎是基本人权';
console.log(motto.length); // 9 → 每个字都是尊严
```

### 2. 字符提取
```javascript
// 下标访问
console.log(motto[2]);    // '拉' → 第三个字符
console.log(motto.charAt(2)); // '拉' → 官方推荐姿势
```

### 3. 大小写变身
```javascript
let companySlogan = 'Always Slacking';
console.log(companySlogan.toUpperCase()); // 'ALWAYS SLACKING' → 土豪金
console.log(companySlogan.toLowerCase()); // 'always slacking' → 低调灰
```

---

## 高级操作秘籍 📚

### 1. 精准定位
```javascript
// 查找字符位置
console.log(motto.indexOf('人')); // 7 → 第8个字符
console.log(motto.lastIndexOf('是')); // 4 → 最后出现位置
```

### 2. 花式截取
```javascript
// 正数截取
console.log(motto.substring(2, 5)); // '拉屎是' → 传统手艺
// 负数截取
console.log(motto.slice(-6, -3));  // '屎是基' → 摸鱼式截取
```

### 3. 美容整形
```javascript
// 去除首尾空格
let dirtyStr = '   请假理由：头痛   ';
console.log(dirtyStr.trim()); // '请假理由：头痛'

// 文字替换
console.log(motto.replace('带薪', '有偿')); // '有偿拉屎是基本人权'
```

### 4. 智能检测
```javascript
console.log(motto.includes('摸鱼')); // false → 老板查岗
console.log(motto.startsWith('带薪')); // true → 职场真理
```

### 5. 分尸大法
```javascript
const workReport = '上班-刷微博-带薪拉屎-假装加班';
console.log(workReport.split('-')); 
// ['上班', '刷微博', '带薪拉屎', '假装加班']
```

---

## 生存法则 ⚔️

1. **模板字面量优先**：告别+号拼接的地狱
2. **善用includes**：比indexOf更直观
3. **正则搭配**：复杂操作请出正则表达式
4. **注意编码**：处理emoji时小心长度计算

> 下集预告：数组の千层套路——从青铜到王者的进化史

💡 记住：字符串就像橡皮泥——掌握方法才能捏出想要的样子！ 🎨 