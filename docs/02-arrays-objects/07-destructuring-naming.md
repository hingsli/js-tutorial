## JavaScript解构赋值从入门到上头 📦

各位代码拆弹专家注意！今天我们要解锁对象的"拆快递"技巧，准备好成为解构大师了吗？🔪

---

### 🕶️ 对象属性偷懒大法

当变量名和属性名相同时，可以这样偷懒：
```javascript
const firstName = 'John';
const lastName = 'Doe';
const age = 30;

// 传统写法（老实人版）
const person = {
  firstName: firstName,
  lastName: lastName,
  age: age
};

// 偷懒写法（聪明人版）
const person = { firstName, lastName, age };

console.log(person.age); // 30（效果一样香）
```

---

### 🧳 对象解构拆包术

**基础拆包：**
```javascript
const todo = {
  id: 1,
  title: '倒垃圾',
  user: {
    name: 'John'
  }
};

// 普通拆包
const { id, title } = todo;
console.log(id); // 1

// 重命名拆包（给快递贴新标签）
const { id: todoId } = todo;
console.log(todoId); // 1

// 套娃拆包（拆开快递里的快递）
const { user: { name } } = todo;
console.log(name); // "John"
```

---

### 🧩 数组解构与剩菜打包

**基础拆法：**
```javascript
const numbers = [23, 67, 33, 49, 52];

// 按顺序拆包
const [first, second] = numbers;
console.log(first, second); // 23 67

// 跳过元素（用逗号占位）
const [first, , third] = numbers;
console.log(first, third); // 23 33

// 打包剩菜（...rest操作符）
const [first, second, ...rest] = numbers;
console.log(rest); // [33, 49, 52]（剩菜真香）
```

---

### 💡 冷知识时间

- **解构顺序**：数组解构像排队领盒饭，先到先得
- **默认值**：可以设置默认值防止拆到undefined（后面会讲）
- **别名技巧**：解构时重命名解决命名冲突问题
- **混合操作**：可以同时解构对象和数组（左右开弓）

---

### 🎯 下集预告

下次我们将解锁：
- JSON

记住：解构就像拆快递，拆得越熟练，代码越简洁！🚀