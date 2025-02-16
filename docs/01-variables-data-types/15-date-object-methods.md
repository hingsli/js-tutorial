# Date对象の摸鱼宝典 📅——时间操作终极奥义

## 基础操作篇

### 1. 时间拆解术
```javascript
const 摸鱼时间 = new Date();

// 获取老板查岗时间
console.log(摸鱼时间.getFullYear());  // 2023 → 当前年份
console.log(摸鱼时间.getMonth() + 1); // 7 → 月份要+1（反人类设计！）
console.log(摸鱼时间.getDate());      // 15 → 当月第几天
console.log(摸鱼时间.getDay());       // 3 → 周三（0=周日开始）
```

### 2. 精确到毫秒的摸鱼
```javascript
console.log(摸鱼时间.getHours());    // 15 → 下午三点
console.log(摸鱼时间.getMinutes());  // 30 → 摸鱼30分钟
console.log(摸鱼时间.getSeconds());  // 45 → 假装在工作
console.log(摸鱼时间.getMilliseconds()); // 250 → 摸鱼手速
```

---

## 花式格式化 ✨

### 1. 国际摸鱼格式
```javascript
// 美式摸鱼（MM/DD/YY）
console.log(Intl.DateTimeFormat('en-US').format(摸鱼时间)); // "7/15/2023"

// 英式摸鱼（DD/MM/YY）
console.log(Intl.DateTimeFormat('en-GB').format(摸鱼时间)); // "15/07/2023"
```

### 2. 摸鱼专用格式
```javascript
// 获取完整月份名（适合写周报）
console.log(Intl.DateTimeFormat('default', { month: 'long' }).format(摸鱼时间)); // "七月"

// 获取缩写月份（适合偷懒）
console.log(摸鱼时间.toLocaleString('default', { month: 'short' })); // "7月"
```

---

## 摸鱼生存指南 ⚔️

### 1. 完美摸鱼时间格式
```javascript
const 摸鱼报告 = 摸鱼时间.toLocaleString('default', {
  weekday: 'long',     // 星期全称
  year: 'numeric',     // 数字年份
  month: 'long',       // 月份全称
  day: 'numeric',      // 日期数字
  hour: '2-digit',     // 两位数小时
  minute: '2-digit',   // 两位数分钟
  timeZone: 'Asia/Shanghai' // 中国时区
});

// 输出："2023年7月15日 星期六 15:30"
```

### 2. 时间戳转换秘籍
```javascript
// 记录摸鱼开始时间
const 摸鱼开始时间戳 = 摸鱼时间.getTime();

// 时间戳还原现场
const 摸鱼现场还原 = new Date(摸鱼开始时间戳);
```

---

## 生存法则 🚨

1. **月份从0开始**：1月是0，12月是11（JS特色）
2. **getDay()陷阱**：0=周日，6=周六
3. **时区敏感操作**：永远明确指定时区
4. **性能优化**：频繁操作建议使用时间戳

> 下集预告：异步编程の奥义——从setTimeout到Promise

💡 记住：时间就像海绵里的水——用Date对象挤一挤，总能摸出鱼来！ 🐟 