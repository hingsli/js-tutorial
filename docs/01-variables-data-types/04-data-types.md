# 数据类型の奇幻漂流 🌊——从青铜到铂金的类型之旅

## 原始类型七兄弟（值类型）

### 1. 字符串（String）—— 话痨担当
```javascript
const greeting = 'Hello World'; // 单双引号皆可
const pickupLine = `你好呀~`;    // 反引号开启模板字符串模式
typeof greeting; // "string"
```

### 2. 数字（Number）—— 精算师
```javascript
const age = 18;       // 整数
const temperature = 36.5;     // 小数
const balance = -5000;    // 负数
typeof age; // "number"（JS没有int/float之分）
```

### 3. 布尔（Boolean）—— 二哈性格
```javascript
const isSingle = true;  
const hasPartner = false;
typeof isSingle; // "boolean"
```

### 4. Null —— 空气型男友
```javascript
const girlfriend = null; // 明确表示"空值"
typeof girlfriend; // "object"（史上最著名bug！）
```

### 5. Undefined —— 薛定谔的变量
```javascript
let boyfriend;
typeof boyfriend; // "undefined"（未定义的痛）
```

### 6. Symbol —— 高冷贵族
```javascript
const id = Symbol('唯一标识符');
typeof id; // "symbol"（独一无二の存在）
```

### 7. BigInt —— 大数恐惧症克星
```javascript
const universeAtomCount = 123456789012345678901234567890n;
typeof universeAtomCount; // "bigint"（n结尾显身份）
```

---

## 引用类型三巨头（对象类型）

### 1. 对象（Object）—— 百变星君
```javascript
const worker = {
  name: '张三',
  skills: ['摸鱼', '带薪拉屎'],
  balance: -5000
};
typeof worker; // "object"
```

### 2. 数组（Array）—— 收纳达人
```javascript
const slackingMethods = ['刷微博', '装开会', '带薪拉屎'];
typeof slackingMethods; // "object"（数组也是对象哦）
```

### 3. 函数（Function）—— 工具人
```javascript
function overtime() {
  console.log('今晚通宵！');
}
typeof overtime; // "function"（本质是特殊对象）
```

---

## 类型冷知识 ❄️

### 动态类型 vs 静态类型
- **JS是变色龙**：变量类型随时变（`let salary = '穷' → salary = 0`）
- **TS是班主任**：TypeScript会严格检查类型（`salary = '富' // 报错！`）

### 存储方式玄学
- **原始类型**：直接存值（像U盘——随身携带）
- **引用类型**：存内存地址（像云盘——随用随取）

### 类型检测骚操作
```javascript
// null检测要特殊处理
const isNull = (val) => val === null;

// 数组检测
Array.isArray(slackingMethods); // true
```

---

> 下集预告：内存の奇妙冒险——栈与堆的爱恨情仇！

💡 记住：原始类型像矿泉水——直接喝，引用类型像奶茶——用吸管（指针）喝。类型就像MBTI——了解清楚才能更好相处！ 🧋