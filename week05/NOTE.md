# 第五周学习总结

## 1. CSS计算 |  收集CSS规则

1. 解析style标签
2. 解析link标签
3. 使用css包解析

```javascript
// 安装css，解析器
// 解析文本，将其放到rules规则容器中
const ast = css.parse(text);
rules.push(...ast.stylesheet.rules);
```

## 2. CSS计算 | 添加调用

1. 当创建一个元素后，立即计算CSS
2. 理论上，当我们分析一个元素时，所有CSS规则已经收集完毕
3. 忽略body里的style标签

## 3. CSS计算 | 获取父元素序列

选择器是跟父元素相关

```javascript
stack.slice().reverse()
```

1. 必须知道元素的所有父元素才能判断元素与规则是否匹配
2. stack获取所有父元素
3. 获得和计算父元素的匹配顺序是从内向外

## 4. CSS计算 | 选择器与元素的匹配

复杂选择器由空格构成，复合选择器针对于一个元素



