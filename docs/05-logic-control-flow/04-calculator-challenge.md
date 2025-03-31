# 计算器挑战

**任务说明：**

创建一个名为 `calculator` 的函数，该函数接收三个参数：`num1`（数字1）、`num2`（数字2）和 `operator`（运算符）。运算符可以是 `+`、`-`、`*` 或 `/`。函数应返回计算结果，如果传入非上述四种运算符，则返回错误信息。

**示例：**

```
calculator(5, 2, '+') // 返回 7
calculator(5, 2, '-') // 返回 3
calculator(5, 2, '*') // 返回 10
calculator(5, 2, '/') // 返回 2.5
calculator(5, 2, '&') // 返回错误信息
```

**提示：**

- 可以使用if语句处理运算符，但这也是使用switch语句的好例子

<details>
  <summary>点击查看解决方案</summary>

```JavaScript
function calculator(num1, num2, operator) {
let result;
switch (operator) {
  case '+':
    result = num1 + num2;
    break;
  case '-':
    result = num1 - num2;
    break;
  case '*':
    result = num1 * num2;
    break;
  case '/':
    result = num1 / num2;
    break;
  default:
    result = '无效运算符';
}
console.log(result);
return result;
}

calculator(3, 4, '*'); // 返回 12
```

</details>
