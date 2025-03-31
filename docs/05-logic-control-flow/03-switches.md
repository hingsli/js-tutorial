# 平行宇宙的开关法官 —— switch 结构

在多重`if...else if`的世界，你或许还觉得太繁琐？试试“开关法官”——`switch`语句，一次性罗列所有可能性，让判决更一目了然。

## 基础开关式审判 🎛️

```javascript
const crimeDegree = '严重';

switch (crimeDegree) {
  case '轻微':
    console.log('处罚：警告并罚款');
    break;
  case '中等':
    console.log('处罚：中等刑罚');
    break;
  case '严重':
    console.log('处罚：重刑伺候');
    break;
  default:
    console.log('未定义的犯罪级别');
    break;
}
```

- `switch`会根据`case`匹配值，一旦匹配成功就执行对应代码。  
- 如果没有手动`break`，会继续执行下一个`case`的代码（**贯穿特性**）。  
- `default`是所有情况都不匹配时的“兜底”处理。

### 贯穿陷阱 🚧

```javascript
const day = 'Monday';

switch (day) {
  case 'Monday':
    console.log('开庭审判');
    // 没有break，继续向下执行
  case 'Tuesday':
    console.log('书面调查');
    break;
  default:
    console.log('暂无日程');
}
```
> 如果忘记`break`，可能会导致“意外的连带执行”。

---

## switch 还是 if？🤔

1. **变量类型**：`switch`适合处理离散的整型或字符串值；复杂区间判断用`if`更好。  
2. **可读性**：当条件太多、且都基于同一变量，`switch`会更直观。  
3. **贯穿特性**：熟悉后可利用贯穿特性做一些巧妙逻辑，但更常见的是加`break`防止出错。

> 下集预告：Calculator Challenge——成为判官，你来算刑期！  