# 函数变形记 🎭——声明与表达式的爱恨情仇

## 函数声明 vs 表达式 🥊

### 霸道总裁（函数声明）
```javascript
function addDollarSign(value) { // 天生贵族，自带皇冠
  return '$' + value;
}
console.log(addDollarSign(100)); // $100 → 随时听候差遣
```

### 社畜打工人（函数表达式）
```javascript
const addPlusSign = function(value) { // 需要先签劳动合同
  return '+' + value;
};
console.log(addPlusSign(200)); // +200 → 签完合同才能干活
```

---

## 变量提升宫斗剧 👑

### 霸道总裁的特权
```javascript
console.log(addDollarSign(300)); // $300 → 先斩后奏！
function addDollarSign(value) {
  return '$' + value;
}
```

### 社畜的悲惨命运
```javascript
console.log(addPlusSign(400)); // ❌ 未初始化就使唤！
const addPlusSign = function(value) {
  return '+' + value;
};
```

---

## 生存法则 ⚔️

1. **声明像霸道总裁**：随时召唤（提升特权）
2. **表达式像社畜**：先定义后使用（遵守劳动法）
3. **分号是社畜的卖身契**：表达式结尾必须带分号
4. **代码整洁之道**：函数集中放顶部，方便管理

> 下集预告：箭头函数来袭——打工人的逆袭 💪

💡 记住：函数就像员工——声明是空降领导，表达式是合同工！ 👔