## JSON从入门到真香 🌟

各位数据搬运工注意！今天我们要解锁JavaScript的"数据翻译官"——JSON，准备好成为数据转换大师了吗？🔄

---

### 🧐 JSON是什么？

- **全称**：JavaScript Object Notation（JavaScript对象表示法）
- **特点**：轻量级、易读、跨语言
- **用途**：前后端数据交换的"普通话"
- **名言**："XML太啰嗦，JSON真香！" —— 前端程序员

---

### 🔄 JSON与JS对象互转

**1. 对象转JSON（序列化）**
```javascript
const post = {
  id: 1,
  title: '文章一',
  body: '正文内容'
};

// 对象 → JSON字符串
const str = JSON.stringify(post);
console.log(str); 
// 输出：{"id":1,"title":"文章一","body":"正文内容"}
```

**2. JSON转对象（反序列化）**
```javascript
// JSON字符串 → 对象
const obj = JSON.parse(str);
console.log(obj.title); // "文章一"
```

---

### 💡 JSON使用小贴士

- **键名必须双引号**：`{"name": "John"}` ✅ vs `{name: "John"}` ❌
- **值类型限制**：支持字符串、数字、布尔、数组、对象、null
- **数组处理**：同样支持序列化/反序列化

```javascript
const posts = [
  { id: 1, title: '文章一' },
  { id: 2, title: '文章二' }
];

const str2 = JSON.stringify(posts);
// 输出：[{"id":1,"title":"文章一"},{"id":2,"title":"文章二"}]
```

---

### 🚨 常见踩坑点

- **直接访问JSON字符串属性**会得到undefined
```javascript
console.log(str.id); // undefined（需要先parse）
```

- **本地存储**只能存字符串，存对象前记得stringify
```javascript
// 正确姿势
localStorage.setItem('post', JSON.stringify(post));
const savedPost = JSON.parse(localStorage.getItem('post'));
```

---

### 🌍 真实世界应用

- **API交互**：如GitHub API返回的JSON数据
- **配置文件**：如package.json
- **数据存储**：本地存储、数据库存储

试试访问 [GitHub用户API](https://api.github.com/users) 看看返回的JSON数据吧！

---

记住：JSON是程序员的通用语言，掌握它就能和全世界的数据对话！🌍