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

1.  选择器从当前元素向外排列
2. 复杂选择器拆成针对单个元素的选择器，循环匹配父元素队列

## 5. CSS计算 | 计算选择器与元素匹配

1. 根据选择器的类型和元素属性，计算是否与当前元素匹配
2. 实现基本选择器，复合选择器由简单选择器构成，id、class、tagName选择器

## 6. CSS计算 | 生成computed属性

1. 元素匹配上，将style逐条覆盖，未根据优先级赋值

## 7. CSS计算 | specificity优先级的计算逻辑

```
inline id class tag
1. div div #id 
   [0, 1, 0, 2]   
2. div #my #id
   [0, 2, 0, 1] 高于第一条规则
3. div .cls #id
   [0, 1, 1, 1]  高于1小于2   
```

1. CSS规则根据specificity和后来优先规则覆盖
2. specificity是个四元组，越左边权重越高
3. 一个CSS规则的specificity根据包含的简单选择器想加而成

## 8 . 排版 | 根据浏览器属性进行排版