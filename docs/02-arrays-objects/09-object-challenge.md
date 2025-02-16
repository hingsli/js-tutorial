# 对象操作挑战

### 步骤 1

创建名为 `library` 的对象数组，包含 3 个对象。每个对象需包含：
- `title` 书名（字符串）
- `author` 作者（字符串）
- `status` 状态对象：
  - `own` 拥有状态（true）
  - `reading` 正在阅读（false）
  - `read` 已读状态（false）

### 步骤 2

将全部书籍的 `read` 状态设为 true（使用点操作符修改，不要直接修改原对象）

### 步骤 3

解构第一本书的标题并重命名为 `firstBook`

### 步骤 4

将 library 对象转为 JSON 字符串

<details>
  <summary>点击查看答案</summary>

### 步骤 1 答案

```js
const library = [
  {
    title: '未来之路',
    author: '比尔·盖茨',
    status: {
      own: true,
      reading: true,
      read: false,
    },
  },
  {
    title: '史蒂夫·乔布斯传',
    author: '沃尔特·艾萨克森',
    status: {
      own: true,
      reading: false,
      read: false,
    },
  },
  {
    title: '饥饿游戏3：嘲笑鸟',
    author: '苏珊·柯林斯',
    status: {
      own: true,
      reading: false,
      read: true,
    },
  },
];
```

### 步骤 2 答案

```js
library[0].status.read = true;
library[1].status.read = true;
library[2].status.read = true;
```

### 步骤 3 答案

```js
const { title: firstBook } = library[0];
console.log(firstBook); // "未来之路"
```

### 步骤 4 答案

```js
const libraryJSON = JSON.stringify(library);
console.log(libraryJSON);
```

</details>
