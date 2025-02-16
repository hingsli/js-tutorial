## JavaScript数组套娃与合体术 🪆

各位数组魔法师注意！今天我们要玩转数组的"套娃"和"合体"绝技，准备好开启多维空间之旅了吗？🚀

---

### 🪆 套娃艺术（嵌套数组）

```javascript:03-array-nesting-concat-spread/script.js
const fruits = ['苹果', '梨子', '橙子'];
const berries = ['草莓', '蓝莓', '树莓'];

// 套娃操作：把浆果数组塞进水果数组
fruits.push(berries);
// 现在水果数组变成：['苹果', '梨子', '橙子', ['草莓', '蓝莓', '树莓']]

// 取出蓝莓的秘技
x = fruits[3][1]; // "蓝莓"

// 创建双层套娃数组
const allFruits = [fruits, berries];
x = allFruits[1][2]; // "树莓"
```

---

### 🧩 合体大法

**方法一：concat拼接术**
```javascript:03-array-nesting-concat-spread/script.js
// 传统拼接（像拼火车）
x = fruits.concat(berries); 
// ['苹果', '梨子', '橙子', '草莓', '蓝莓', '树莓']
```

**方法二：展开运算符(...)**
```javascript:03-array-nesting-concat-spread/script.js
// 现代展开（像烟花绽放）
x = [...fruits, ...berries]; 
// 效果同上，但更酷炫！
```

---

### 🏋️ 降维打击（扁平化数组）

```javascript:03-array-nesting-concat-spread/script.js
const 多维数组 = [1, 2, [3, 4, 5], 6, [7, 8]];
x = 多维数组.flat(); 
// [1, 2, 3, 4, 5, 6, 7, 8]（三维变一维）
```

---

### 🛠️ 静态方法工具箱

**1. 验明正身：Array.isArray()**
```javascript:03-array-nesting-concat-spread/script.js
x = Array.isArray(fruits); // true（是数组本尊）
x = Array.isArray('假装数组'); // false（李鬼现形）
```

**2. 点石成金：Array.from()**
```javascript:03-array-nesting-concat-spread/script.js
x = Array.from('12345'); 
// ['1', '2', '3', '4', '5']（字符串变数组）
```

**3. 聚沙成塔：Array.of()**
```javascript:03-array-nesting-concat-spread/script.js
const a = 1, b = 2, c = 3;
x = Array.of(a, b, c); 
// [1, 2, 3]（散装变量变数组）
```

---

### 🧠 冷知识时间

- **套娃深度**：理论上可以无限套娃，但建议别超过3层，否则容易"晕数组"😵
- **展开运算符**：不仅能展开数组，还能用于对象（后面会讲）
- **扁平化**：flat()默认只展开一层，想彻底展开可以用flat(Infinity)

---

### 🎯 下集预告

下次我们将迎来：
- 数组挑战赛（检验学习成果）
- 高阶数组方法（filter/map/reduce三巨头）
- 更多骚操作...

记住：数组就像俄罗斯套娃，套得越深，功力越深！💪