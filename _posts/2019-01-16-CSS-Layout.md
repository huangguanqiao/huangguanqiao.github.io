---
layout:     post
title:    CSS layout
subtitle:   BY Guanqiao Huang
date:       2019-01-16
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CSS
---
# CSS Float
## Example 1
```CSS
.left{
    float: left;
    width:50%;
}

.right{
    float:left;
    width:50%;
}

.container{
    overflow:auto; 
    /*或者overflow:hidden
    这样变成Block Formatting Context*/

}
```

## Example 2
```CSS
.container::after{
    content: '';
    clear: both;
    display: block;
}
```

## Example 3
html中加入<div class="clearfix"></div>
```CSS
.clear{
    clear:both;
}
```

## Example 4
```CSS
/*设定BFC另一种方法*/
.container{
    display:flow-root;
}
```

# CSS Grid

## Example 1
```html
<div id="grid-container">
    <div class="cell-1"></div>
    <div class="cell-2"></div>
    <div>

```

```CSS
#grid-container{
    display: grid;
    width: 500px;
    height: 500px;
    background-color: grey;
    grid-template-rows: 100px 100px 100px 100px 100px;
    grid-template-columns: 100px 100px 100px 100px 100px;
}

.cell-1{
    background-color: blue;
    grid-row: 1 / 3;
    grid-column: 1 /3;
    /* this is equal to
    grid-area: 1 / 1 / 4 / 3 ;

    /*grid-column: 2 /span 3;
    this means start form 2 and span 3 block"*/

}

.cell-2{
    background-color: blue;
}
```

## Example 2
```CSS
#grid-container{
    display: grid;
    width: 500px;
    height: 500px;
    background-color: grey;
    grid-template-rows: [Y1]100px [Y2]100px [Y3]100px [Y4]100px [Y5]100px;
    grid-template-columns: [X1]100px [X2]100px [X3]100px [X4]100px [X5]100px;
}

.cell-2{
    background-color: blue;
    grid-row: Y2 / Y4;
    grid-column: X1 / X6;
}
```

## Example 3
```CSS
#grid-container{
    display: grid;
    width: 500px;
    height: 500px;
    background-color: grey;
    grid-template-rows: [Y1]100px [Y2]100px [Y3]100px [Y4]100px [Y5]100px;
    grid-template-columns: [X1]100px [X2]100px [X3]100px [X4]100px [X5]100px;
    grid-template-areas: "header header header header header"
    "nav main main main main"
    "nav main main main main"
    "nav main main main main"
    ". footer footer footer ." ;

}

.cell-2{
    background-color: blue;
    grid-area: header;
}
```

## Example 4
```CSS
#grid-container{
    display: grid;
    width: 540px;
    height: 540px;
    background-color: grey;
    grid-template-rows: [Y1]100px [Y2]100px [Y3]100px [Y4]100px [Y5]100px;
    grid-template-columns: [X1]100px [X2]100px [X3]100px [X4]100px [X5]100px;
    grid-template-areas: "header header header header header"
    "nav main main main main"
    "nav main main main main"
    "nav main main main main"
    ". footer footer footer ." ;
    row-gap: 10px;
    column-gap: 10px;s
}

.cell-2{
    background-color: blue;
    grid-area: header;
}
```

## Example 5
```CSS
#grid-container{
    display: grid;
    width: 540px;
    height: 540px;
    background-color: grey;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
    grid-template-columns: repeat(5,1fr);
    /*1fr代表一份*/
    grid-template-areas: "header header header header header"
    "nav main main main main"
    "nav main main main main"
    "nav main main main main"
    ". footer footer footer ." ;
    row-gap: 10px;
    column-gap: 10px;s
}

.cell-2{
    background-color: blue;
    grid-area: header;
}
```


# Flexbox
```CSS
.flex-container{
    display: flex;
    height: 300px;
    flex-direction: row;
    /*水平置中对齐，还有flex-start和flex-end，代表起始方向和结束方向*/
    justify-content: center; 
    align-items: center; /*垂直置中对齐*/
    /*flex-wrap是设置要不要分行，默认nowrap, 改成wrap就是可以分行 */
    flex-wrap: nowrap;
    flex-flow: column wrap; /*这是direction和wrap的结合*/
    align-content: space-around; /*这是flex-item多于一行的显示方式 对齐效果*/
}

.box{
    /*这是排序，默认是0，可填-1或者1*/
    order:0;
    /*用法和align-item一样，只不过用在子container里， 用在个别情况*/
    align-self:flex-start;
    /*basis设定flex的高度或者宽度，看direction的情况, 原有的高度或宽度设定会失效*/ 
    flex-basis: 100px; 
    /*grow扩大比例，意思是所有内容 宽度或者高度 加起来的数值和容器总数值一样. 计算方式是剩余空间除以多少等份量，再加到子容器中，0是保持原有大小*/
    flex-grow: 1;
    /*shrink缩小比例，假如超出了container，如何缩小，这个和grow相反。默认是1，0的话是不缩小*/
    flex-shrink：1；
    /*这是grow，shrink，basis的结合, 1 1 auto意思是平均分配空间，子element同步变大或者缩小*/
    flex：1 1 auto;
}
```

### 实用例子
用ul li建立列表快速建立， ul>li*5>a[href='#]{$}
```

```

# FlexBox
## justify-content
Below are five commonly used values for the justify-content property:

- flex-start — all items will be positioned in order, starting from the left of the parent container, with no extra space between or before them.
- flex-end — all items will be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.
- center — all items will be positioned in order, in the center of the parent container with no extra space before, between, or after them.
- space-around — items will be positioned with equal space before and after each item, resulting in double the space between elements.
- space-between — items will be positioned with equal space between them, but no extra space before the first or after the last elements.

```CSS
.container {
  display: flex;
  justify-content: flex-end;
}
```

## align-items
Below are five commonly used values for the align-items property:

- flex-start — all elements will be positioned at the top of the parent container.
- flex-end — all elements will be positioned at the bottom of the parent container.
- center — the center of all elements will be positioned halfway between the top and bottom of the parent container.
- baseline — the bottom of the content of all items will be aligned with each other.
- stretch — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).

## Review: Flexbox
1. display: flex changes an element to a block-level container with flex items inside of it.
2. display: inline-flex allows multiple flex containers to appear inline with each other.
3. justify-content is used to space items along the main axis.
- flex-end will set all items to be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.
4. align-items is used to space items along the cross axis.
- The align-items property makes it possible to space out flex items vertically.
5. flex-grow is used to specify how much space (and in what proportions) flex items absorb along the main axis.
6. flex-shrink is used to specify how much flex items shrink and in what proportions along the main axis.
7. flex-basis is used to specify the initial size of an element styled with flex-grow and/or flex-shrink.
8. flex is used to specify flex-grow, flex-shrink, and flex-basis in one declaration.
- The flex property can have two values to declare either the flex-grow and flex-shrink properties or the flex-grow and flex-basis properties.
- When there are only two values of the flex property, the first value is used to set flex-grow.
9. flex-wrap specifies that elements should shift along the cross axis if the flex container is not large enough.
10. align-content is used to space rows along the cross axis.
11. flex-direction is used to specify the main and cross axes.
12. flex-flow is used to specify flex-wrap and flex-direction in one declaration.
13. Flex containers can be nested inside of each other by declaring display: flex or display: inline-flex for children of flex containers.
- inline-flex allows us to create flex containers that are also inline elements.
- Given there is enough space, the .box elements will have the width of 300px, but if not, they will shrink to fit the screen.