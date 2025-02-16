# 首字母大写挑战赛 🏆

**任务说明**：

把变量 `myString` 的首字母变成大写，用我们上节课教过的那些骚操作。把结果存到 `myNewString` 变量里。

欢迎解锁多重姿势解题 😏

**预期效果**：

```JavaScript
const myString = 'developer';

console.log(myNewString); // 期待输出 'Developer'
```

**友情提示**：

1. 可以用 `charAt()` 或者简单粗暴的 `字符串[索引]` 来获取首字母
2. `.toUpperCase()` 能让字母集体变身高富帅
3. `substring()` 和 `slice()` 可以帮你偷字符串的片段

<details>
  <summary>点我看答案（乖，先自己试试）</summary>
  
  解法千千万，这里抛砖引玉：

```JavaScript
// 方案 1（老实人版）
const myNewString = myString.charAt(0).toUpperCase() + myString.substring(1);

// 方案 2（装逼版：直接用下标访问）
const myNewString = myString[0].toUpperCase() + myString.substring(1);

// 方案 3（模板字符串爱好者）
const myNewString = `${myString[0].toUpperCase()}${myString.slice(1)}`;
```

核心思路：先抓首字母来个大写，然后拼接上字符串的剩余部分（用 `substring()` 或 `slice()` 截取）。举个栗子🌰：就像给单词戴了个大写字母的帽子 🎩

</details>