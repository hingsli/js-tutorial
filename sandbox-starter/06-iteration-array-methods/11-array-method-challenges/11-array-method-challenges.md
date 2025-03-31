# 数组方法挑战

## 挑战 1

**说明：**

使用 `people` 数组创建一个名为 `youngPeople` 的新数组，该数组应只包含 25 岁及以下人员的对象，且对象中只保留 `name` 和 `email` 属性。`name` 属性应由人员的姓和名组合而成。

```JavaScript
const people = [
  {
    firstName: 'John',
    lastName: 'Doe',
    email: 'john@gmail.com',
    phone: '111-111-1111',
    age: 30,
  },
  {
    firstName: 'Jane',
    lastName: 'Poe',
    email: 'jane@gmail.com',
    phone: '222-222-2222',
    age: 25,
  },
  {
    firstName: 'Bob',
    lastName: 'Foe',
    email: 'bob@gmail.com',
    phone: '333-333-3333',
    age: 45,
  },
  {
    firstName: 'Sara',
    lastName: 'Soe',
    email: 'Sara@gmail.com',
    phone: '444-444-4444',
    age: 19,
  },
  {
    firstName: 'Jose',
    lastName: 'Koe',
    email: 'jose@gmail.com',
    phone: '555-555-5555',
    age: 23,
  },
];
```

**预期结果：**

```JavaScript
console.log(youngPeople);

[
  {name: 'Jane Poe', email:'jane@gmail.com'},
  {name: 'Sara Soe', email:'sara@gmail.com'},
  {name: 'Jose Koe', email:'jose@gmail.com'}
]
```

<details>
  <summary>点击查看解答</summary>

```JavaScript
const youngPeople = people
  .filter((person) => person.age <= 25)
  .map((person) => ({
    name: person.firstName + ' ' + person.lastName,
    email: person.email,
  }));
```

</details>

## 挑战 2

**说明：**

计算数组中所有正数的和。

**预期结果：**

```JavaScript
const numbers = [2, -30, 50, 20, -12, -9, 7];

console.log(positiveSum); // 79
```

<details>
  <summary>点击查看解答</summary>
  
```JavaScript
const numbers = [2, -30, 50, 20, -12, -9, 7];

const positiveSum = numbers
  .filter((number) => number > 0)
  .reduce((acc, cur) => acc + cur, 0);

console.log(positiveSum);
```
 
</details>

## 挑战 3

**说明：**

创建一个名为 `capitalizedWords` 的新数组，将原数组中的每个单词首字母大写。

**预期结果：**

```JavaScript
const words = ['coder', 'programmer', 'developer'];

console.log(capitalizedWords); // ['Coder', 'Programmer', 'Developer']
```

**提示：**

回忆前面几节的内容，我们有一个将字符串首字母大写的挑战。这里你正在对数组中的每个单词做同样的事情。

<details>
  <summary>点击查看解答</summary>
  
```JavaScript
const capitalizedWords = words.map(
  (word) => word[0].toUpperCase() + word.slice(1, word.length)
);
```
</details>
