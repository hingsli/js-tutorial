# 浏览器控制台生存指南 🕹️

各位前端/全栈萌新注意！这个视频要带你们解锁程序员最强摸鱼工具——浏览器控制台！（老板来了记得Alt+Tab）

## 控制台の正确打开方式
- **召唤姿势**：
  - Mac：`⌘ + Option + J` 
  - Windows：`F12` 或 `Ctrl + Shift + J`
- **清屏秘籍**：
  - 输入`clear()` 
  - 快捷键`Ctrl + L`（Mac用`⌘ + L`）
  - 直接刷新页面（物理清屏法🌚）

## console的108种玩法 🎮
### 基础三连
```javascript
console.log(100); // 输出紫色数字
console.log('救命啊！'); // 白色字符串警告
console.log(20, '混搭', true); // 一次输出三种数据类型
```

### 变量监控室
```javascript
const 我的密码 = '123456'; // 当然实际千万别这么写😂
console.log(我的密码); // 输出变量值
```

### 花式报警器
```javascript
console.error('红色警报！'); // 适合假装系统崩溃
console.warn('黄色警告！'); // 用来吓唬产品经理
```

### 对象变表格
```javascript
console.table({
  名字: '张三', 
  技能: '摸鱼',
  工位: '靠窗第三排'
}); // 把对象变成精致小表格
```

### 分组折叠术
```javascript
console.group('摸鱼证据');
console.log('刷微博');
console.warn('被发现！');
console.groupEnd(); // 把日志打包成折叠组
```

### CSS骚操作
```javascript
const 杀马特样式 = 'padding:10px; background:#000; color:#0f0; font-size:20px;';
console.log('%c葬爱家族欢迎你', 杀马特样式); // 控制台非主流现场
```

## 冷知识彩蛋 🥚
- 在控制台直接运行JS（临时测试用）：
  ```javascript
  1 + 1 // 输出2
  alert('老板来啦！') // 紧急预警
  new Date() // 显示当前时间（加班计时器）
  ```
- VS Code效率技巧：输入`clg`后按Tab键自动生成`console.log()`语句（前端开发必备快捷键）

> 下集预告：代码注释の艺术（以及如何用注释气死同事）& 键盘侠必备快捷键！ ⌨️

---

💡 记住：控制台是程序员的读心术——报错信息会告诉你一切秘密。多摸鱼...啊不，多练习才能成为真正的控制台忍者！ 🐱👤
