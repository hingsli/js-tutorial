# 审判的插播与跳过 —— break 与 continue

在法庭上，有时审判官会紧急喊停（`break`），或跳过当事人不予审理（`continue`）。在 JavaScript 中，这两个关键词也能帮助我们控制循环流程。

## break —— 中止审判

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break; // 一旦符合条件，立即终止循环
  }
  console.log('当前审判编号:', i);
}
```
- 当 `i` 等于 5 时，整个循环就停止了。

## continue —— 跳过当前审判

```javascript
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue; // 对偶数编号直接跳过，不执行后续语句
  }
  console.log('奇数审判编号:', i);
}
```
- 每遇到偶数就会跳过打印逻辑，只输出奇数编号。

## 用法场景

1. **break**：在找到目标或出现特殊情况时，可以提前结束循环。
2. **continue**：略过某些不需要处理的情形，但不影响后面的审判继续进行。

> 下集预告：`while` 与 `do...while`——灵活多变的审判流程！