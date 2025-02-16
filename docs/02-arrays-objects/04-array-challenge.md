# 数组整容术

### 挑战1：数组倒装秀

**任务说明：**

用学过的数组方法给下面这个数组整容成预期效果：

```js
const arr = [1, 2, 3, 4, 5];
```

**想要的效果：**

```js
console.log(arr);
// [6, 5, 4, 3, 2, 1, 0];
```

**友情提示**：别找了，这次没提示，就是这么任性 😏

<details>
  <summary>点击查看美颜方案</summary>
  
  ```js
  const arr = [1, 2, 3, 4, 5];

    arr.unshift(0); // 头部加个0
    arr.push(6);    // 屁股塞个6
    arr.reverse();   // 来个大翻身

    console.log(arr); // [6, 5, 4, 3, 2, 1, 0];
```

</details>


### 挑战2：数组相亲记

**任务说明：**

把`arr1`和`arr2`撮合成新数组`arr3`，注意：

```js
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [5, 6, 7, 8, 9, 10];
```

合并时发现它们都有5这个共同爱好...请让它们保持适当距离（去掉重复的5）

**想要的效果：**

```js
console.log(arr3);
// [1,2,3,4,5,6,7,8,9,10]
```

**友情提示**：concat()、spread操作符、slice()、splice()总有一个适合你

<details>
  <summary>点击查看相亲成功方案</summary>
  
```js
const arr1 = [1, 2, 3, 4, 5];
const arr2 = [5, 6, 7, 8, 9, 10];

// 方案一：简单粗暴法
const arr3 = arr1.slice(0, 4).concat(arr2);

// 方案二：先合体再动刀
const arr4 = [...arr1, ...arr2];
arr4.splice(4, 1); // 第5个位置切一刀

// 两种方案都能得到 [1,2,3,4,5,6,7,8,9,10]
```

</details>

