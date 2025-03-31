# FizzBuzz 挑战

**要求：**

- 打印/记录 1 到 100 的数字
- 遇到 **3的倍数** 时打印 "Fizz" 代替数字
- 遇到 **5的倍数** 时打印 "Buzz"
- 遇到 **同时是3和5的倍数** 时打印 "FizzBuzz"

**提示：**

如果你已经学习到本课程当前阶段，那么你应该知道如何编写循环以及在每次迭代时输出/记录内容。你也知道如何使用 "if/else/else if" 来检查条件。你还知道如何使用取模运算符 (%) 来获取数字的余数。这些知识就足够完成这个挑战了。祝你好运！

<details>
  <summary>点击查看解决方案</summary>

### 方案 1: `For` 循环

```JavaScript
  for (let i = 1; i <= 100; i++) {
    if (i % 15 == 0) {
    	console.log("FizzBuzz");
    } else if (i % 3 == 0) {
    	console.log("Fizz");
    } else if (i % 5 == 0) {
    	console.log("Buzz");
    } else {
    	console.log(i);
    }
}
```

在上述代码中，我们将初始化表达式设为`1`。将条件设置为`i <= 100`。递增表达式设为`i++`。

我们首先检查`i`是否能被**15**整除。因为这意味着`i`同时能被**3**和**5**整除。在这种情况下，我们打印`"FizzBuzz"`。接着检查`i`是否能被**3**整除，如果是则打印`"Fizz"`。然后检查是否能被**5**整除，如果是则打印`"Buzz"`。如果`i`既不能被3也不能被5整除，就打印`i`（当前数字）。

### 方案 2: `While` 循环

```JavaScript
  let i = 1;

  while(i <= 100) {
    if (i % 15 == 0) {
    	console.log("FizzBuzz");
    } else if (i % 3 == 0) {
    	console.log("Fizz");
    } else if (i % 5 == 0) {
    	console.log("Buzz");
    } else {
    	console.log(i);
    }

    i++;
  }
```

这里我们做了同样的事情，只是使用了`while`循环

</details>
