## JavaScript对象字面量从入门到上头 😎

各位代码艺术家注意！今天我们要玩转JavaScript的"百宝箱"——对象字面量！准备好开启键值对的魔法之旅了吗？✨

---

### 🧰 创建你的第一个对象

```javascript
const person = {
  name: '张三',
  age: 30,
  isAdmin: true,
  address: {
    street: '人民路123号',
    city: '北京',
    province: '京',
  },
  hobbies: ['音乐', '运动'],
};
```

---

### 🔍 对象操作四连击

**1. 访问属性**
```javascript
// 点号操作符（推荐）
x = person.name; // "张三"

// 方括号操作符（特殊场景用）
x = person['age']; // 30

// 套娃访问
x = person.address.province; // "京"
x = person.hobbies[0]; // "音乐"
```

**2. 更新属性**
```javascript
person.name = '李四'; // 改名换姓
person['isAdmin'] = false; // 降权处理
```

**3. 删除属性**
```javascript
delete person.age; // 年龄是秘密！🔒
```

**4. 新增属性**
```javascript
person.hasChildren = true; // 喜当爹/妈 👶
```

---

### 🎭 对象的花式玩法

**给对象加个方法**
```javascript
person.greet = function() {
  console.log(`大家好，我是${this.name}！`);
};

person.greet(); // 输出：大家好，我是李四！
```

**多词属性（慎用！）**
```javascript
const person2 = {
  'first name': '小明',
  'last name': '王',
};

x = person2['first name']; // 必须用方括号访问
```

---

### 💡 冷知识时间

- **this关键字**：在方法中指向对象本身（后面会详细讲）
- **动态属性**：可以随时增删改查，比女朋友还善变 💔
- **嵌套深度**：理论上可以无限套娃，但建议别超过3层（会晕对象）

---

### 🚀 下集预告

下次我们将解锁：
- 对象套娃术（对象嵌套对象）
- 展开运算符在对象中的妙用
- 对象的高级玩法...

记住：对象就像百宝箱，装得越多，能力越强！💪