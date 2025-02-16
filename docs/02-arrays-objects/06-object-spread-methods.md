## JavaScript对象扩展操作符与秘籍 📚

各位对象操控大师注意！今天我们要解锁对象的"影分身之术"和"读心术"，准备好成为对象忍者了吗？🥷

---

### 🏗️ 对象构造的两种姿势

**1. 字面量构造（常用）**
```javascript
const todo = {
  id: 1,
  name: '买牛奶',
  completed: false
};
```

**2. 构造函数（怀旧版）**
```javascript
const todo = new Object();
todo.id = 1;
todo.name = '买牛奶';
todo.completed = false;
```

---

### 🪆 对象套娃术

```javascript
const person = {
  address: {
    coords: {
      lat: 42.9384,
      lng: -71.3232
    }
  }
};

x = person.address.coords.lat; // 42.9384（套娃六层照样拿）
```

---

### 🧩 对象合体大法

**方法一：影分身之术（...展开符）**
```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const obj3 = { ...obj1, ...obj2 }; // {a:1, b:2, c:3, d:4}
```

**方法二：传统合体法（Object.assign）**
```javascript
const obj4 = Object.assign({}, obj1, obj2); // 同上，但像用大哥大打电话
```

---

### 📚 对象数组操作

```javascript
const todos = [
  { id: 1, name: '买牛奶' },
  { id: 2, name: '接孩子放学' },
  { id: 3, name: '倒垃圾' }
];

x = todos[0].name; // "买牛奶"（数组里挖对象）
```

---

### 🔍 对象读心术（Object方法）

**1. 偷钥匙（keys）**
```javascript
x = Object.keys(todo); // ['id', 'name', 'completed']
```

**2. 量腰围（length）**
```javascript
x = Object.keys(todo).length; // 3（对象没有腰，得先偷钥匙）
```

**3. 偷宝物（values）**
```javascript
x = Object.values(todo); // [1, '买牛奶', false]
```

**4. 连锅端（entries）**
```javascript
x = Object.entries(todo); 
// [ ['id',1], ['name','买牛奶'], ['completed',false] ]
```

**5. 查户口（hasOwnProperty）**
```javascript
x = todo.hasOwnProperty('age'); // false（年龄是秘密！）
```

---

### 💡 冷知识时间

- **展开符**：ES6新宠，2015年前只能用Object.assign()
- **深浅拷贝**：这两种方法都是"肤浅"的拷贝（浅拷贝）
- **现代编程**：展开符更简洁，但老代码里常见Object.assign()

---

### 🎯 下集预告

下次我们将解锁：
- 解构赋值（对象拆包术）
- 对象与数组的混合双打
- 更高级的对象骚操作...

记住：对象就像百宝箱，掌握方法才能成为真正的宝藏猎人！💰