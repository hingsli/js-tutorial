# 调用栈叠叠乐 🥞——函数执行的叠盘子艺术

## 场景一：顺序执行（单身狗式）

```javascript:11-call-stack/script.js
function first() { console.log('first...'); } // 盘子1
function second() { console.log('second...'); } // 盘子2
function third() { console.log('third...'); } // 盘子3

first();  // 🥞 [first] → 吃完移走
second(); // 🥞 [second] → 吃完移走
third();  // 🥞 [third] → 吃完移走
```

### 叠盘子原理：
1. 放入`first` → 执行 → 移走
2. 放入`second` → 执行 → 移走
3. 放入`third` → 执行 → 移走

---

## 场景二：嵌套调用（俄罗斯套娃式）

```javascript:11-call-stack/script.js
function first() {
  console.log('first...');  // 特工1号
  second(); // 呼叫支援
}

function second() {
  console.log('second...'); // 特工2号
  third();  // 呼叫终极支援
}

function third() {
  console.log('third...');  // 王牌特工
}

first(); // 任务开始！
```

### 特工任务链：
1. 🥞 [first] 开始任务
2. 🥞 [first → second] 请求支援
3. 🥞 [first → second → third] 终极支援
4. 🥞 [first → second] 王牌撤退
5. 🥞 [first] 支援撤退
6. 🥞 任务完成！

---

## 浏览器侦探工具使用指南 🔍

1. 打开开发者工具 → Sources
2. 在`first()`处设置断点 🎯
3. 观察Call Stack区域：
   - 点击步进按钮▶️ 观看函数叠叠乐
   - 嵌套调用时 → 栈越叠越高
   - 函数返回时 → 从栈顶开始拆

![调用栈动图演示](https://media.giphy.com/media/3o7TKMt1VVNkHV2PaE/giphy.gif)

---

## 调用栈生存法则 📜

1. **后进先出原则**：最后进来的函数最先处理（像热乎的煎饼）
2. **单线程强迫症**：一次只能处理一个栈顶任务
3. **嵌套调用警告**：叠太高会触发"栈溢出"警报（Stack Overflow）
4. **调试神器**：用Call Stack回溯函数执行路径

> 下集预告：条件判断大冒险——代码世界的岔路口 🚦

💡 记住：调用栈就像叠盘子——最后放上去的总是最先被处理！ 🥢