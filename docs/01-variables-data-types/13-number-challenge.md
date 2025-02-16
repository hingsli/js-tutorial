# 数字大作战🔢

**任务要求✨：**

创建两个变量：`x`（1-100的随机数）和`y`（1-50的随机数）。然后计算它们的和、差、积、商、余数，并用骚气的格式打印出来！

**效果预览：**

```JavaScript
console.log(sumOutput);       // 如：31 + 15 = 46
console.log(differenceOutput);// 如：31 - 15 = 16 
console.log(productOutput);   // 如：31 * 15 = 465
console.log(quotientOutput);  // 如：31 / 15 ≈ 2.0667
console.log(rmOutput);        // 如：31 % 15 = 1（余数）
```

**小贴士💡：**

1. `Math.random()` 能给你0到1的随机数（但永远得不到1）
2. `Math.floor()` 是数学老师的向下取整大法

<details>
  <summary>点我看答案👀</summary>
  
  ```JavaScript
// 生成两个幸运数字
x = Math.floor(Math.random() * 100) + 1;
y = Math.floor(Math.random() * 50) + 1;

// 加法搞起
const sum = x + y;
const sumOutput = `${x} + ${y} = ${sum}`;
console.log(sumOutput);

// 减法走起  
const difference = x - y;
const differenceOutput = `${x} - ${y} = ${difference}`;
console.log(differenceOutput);

// 乘法安排
const product = x * y;  // 这里偷偷修好了原代码的下划线问题
const productOutput = `${x} * ${y} = ${product}`;
console.log(productOutput);

// 除法警告
const quotient = x / y;
const quotientOutput = `${x} / ${y} = ${quotient}`;
console.log(quotientOutput);

// 余数玄学
const rm = x % y;
const rmOutput = `${x} % ${y} = ${rm}`;
console.log(rmOutput);
```
</details>