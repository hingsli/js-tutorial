# 执行上下文真人秀 🎬——JS代码的幕后人生

## 双面间谍的日常 🕵️

```javascript
const x = 100; // 变量登记处（内存创建阶段：undefined → 100）
const y = 50;   // 另一个待命间谍

function getSum(n1, n2) { // 函数特工档案已存档
  const sum = n1 + n2;    // 秘密任务进行中
  return sum;             // 任务完成，返回总部
}

const sum1 = getSum(x, y);   // 特工第一次出动
const sum2 = getSum(10, 5);  // 换装再战

console.log(sum1, sum2); // 150 15 → 任务报告
```

---

## 执行上下文双阶段大揭秘 🔍

### 1. 内存创建阶段（准备期）
- 🏨 变量酒店开张：`x=undefined`, `y=undefined`
- 📚 函数图书馆建档：`getSum`完整代码存档
- 🧳 行李箱打包：`sum1=undefined`, `sum2=undefined`

### 2. 代码执行阶段（行动期）
| 代码行 | 操作                      | 现场直击 👀               |
|-------|---------------------------|--------------------------|
| 1     | `x = 100`                 | 间谍x领到真实身份证       |
| 2     | `y = 50`                  | 间谍y拿到秘密资金         |
| 7     | 召唤`getSum(x, y)`        | 新建临时作战指挥部 🚨     |
| 4     | `sum = 100 + 50`          | 特工在指挥部内完成计算    |
| 5     | 返回150                   | 指挥部拆除，带着战利品撤退|
| 8     | 再次召唤`getSum(10, 5)`   | 新建二号临时指挥部 🚩     |

---

## 浏览器侦探工具使用指南 🔧

1. 打开开发者工具 → Sources
2. 在`script.js`第一行设置断点 🎯
3. 刷新页面开启侦查模式
4. 使用步进按钮观察：
   - 👉 变量从`undefined`变身真实值
   - 👉 函数调用时新建临时上下文
   - 👉 局部变量在"Local"区域活动

![Debugger演示](./images/debugger.png)

---

## 关键记忆点 🧠

1. **JS是单线程强迫症**：一次只做一件事，做完才接下一单
2. **函数像临时帐篷**：调用时搭起，完成就拆除
3. **全局上下文是总部**：页面关闭才退休
4. **变量出生证**：先拿undefined身份证，执行时才获真实身份

> 下集预告：调用栈迷宫——函数执行的俄罗斯套娃 🪆

💡 记住：执行上下文就像话剧舞台——每个函数都有自己的表演时刻！ 🎭