### 1. display:none、visibility:hidden、opacity:0 三者的异同点
+ 三者都会隐藏对应的元素
+ display:none 对应的元素不会在文档流中占据空间
+ opacity:0 对应元素的事件监听器还会触发
+ visibility:hidden 对应的元素依旧在文档流中占据空间

### 2. 简单选择器
+ div p 后代选择器：选择包含在`<div>`之中的**所有**`<p>`标签
+ div > p 子元素选择器：只选择属于`<div>`**子元素**的`<p>`标签
+ div + p 相邻选择器：选择紧接在`<div>`之后的**第一个同级**`<p>`标签
+ div ~ p 匹配选择器：选择紧接在`<div>`之后的**所有同级**`<p>`标签

### 3. CSS选择器特殊性权重
+ 选择器的特殊性值表述为4个部分，用0,0,0,0表示
    + 行间样式：1,0,0,0
    + ID选择器：0,1,0,0
    + 类选择器、属性选择器、伪类：0,0,1,0
    + 元素：0,0,0,1
    + !important比较特殊，可以将其特殊性理解为：1,0,0,0,0，拥有最高特殊性
+ 当特殊性相同时，后声明的样式会覆盖先声明的样式
+ 伪类遵循爱恨原则(LVHA)，即伪类想要同时生效，需要按照:link :visited :hover :active的顺序排列

### 4. CSS中触发GPU加速的属性
+ transform
+ opacity
+ filter

### 5. 响应式布局
GitHub上有一个讲解非常清晰和详实 https://github.com/forthealllight/blog/issues/13




