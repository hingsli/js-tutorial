# 多重人格审判官 —— else if 结构登场

在上一节中，我们只见过单一条件的审判（`if`）。但现实世界中往往错综复杂，需要更灵活的多重判决。此时，我们的“多重人格审判官”——`else if`就闪亮登场了！

## 多重审判模式 👨⚖️

### 标准多重判断
```javascript
const crimeLevel = 3;

if (crimeLevel === 1) {
  console.log('罪行较轻，缓刑观察。');
} else if (crimeLevel === 2) {
  console.log('中度犯罪，判处有期徒刑。');
} else if (crimeLevel === 3) {
  console.log('严重犯罪，判处无期徒刑。');
} else {
  console.log('恶意度未知，进一步调查！');
}
```
- 如果第一个条件不成立，就会审查第二个条件，以此类推。  
- 一旦匹配到某个条件，后续的判决就不再执行。

### 多重if和嵌套地狱（不推荐）
```javascript
const zhangSan = 80;
const liSi = 75;

if (zhangSan > 60) {
  if (zhangSan > liSi) {
    console.log('张三成绩更好，但都及格了。');
  } else {
    console.log('李四成绩比张三好，但都及格了。');
  }
} else {
  console.log('张三不及格，无法与李四比较。');
}
```
- 多重`if`往往会使结构复杂，对可读性不利。  
- 使用`else if`可以让代码更清晰。

---

## else if 的最佳实践 💡
1. 保持条件清晰：多个分支要相互排斥，不要写相互冲突的条件。  
2. 谨慎嵌套：能用“并列else if”就不用过度嵌套。  
3. 记得用`else`作底线处理：如果所有条件都不满足，`else`作为默认“兜底”。

> 下集预告：Switch判官——用“开关”式思维处理复杂案例！ 