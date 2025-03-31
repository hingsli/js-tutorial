# 流动法官 —— while 与 do...while

除了 `for` 循环，还有两位更灵活的流动法官：`while` 与 `do...while`。它们专注于“在满足条件的前提下”，持续进行审判。

## while 循环

```javascript
let i = 0;
while (i < 5) {
  console.log('while 审判：第' + i + '次');
  i++;
}
```
- **先检查条件**，再决定是否执行循环体。
- 如果初始条件就是 `false`，循环体可能一次都不执行。

## do...while 循环

```javascript
let j = 0;
do {
  console.log('do...while 审判：第' + j + '次');
  j++;
} while (j < 5);
```
- **先执行一次循环体**，然后再检查条件。
- 无论条件是否成立，循环体都会至少执行一次。

## 对比选择

- `while` 适合先判断后执行，可能执行 0 次。
- `do...while` 保证至少执行 1 次。

> 下集预告：FizzBuzz Challenge——经典循环挑战，检验你的审判技巧！