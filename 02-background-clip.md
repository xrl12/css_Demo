# background-clip的使用

## 介绍

`background-clip` 设置元素的背景（背景图片或颜色）是否延伸到边框、内边距盒子、内容盒子下面。

**如果没有设置背景图片（[`background-image`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-image)）或背景颜色（[`background-color`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/background-color)），那么这个属性只有在边框（ [`border`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border)）被设置为非固实（soild）、透明或半透明时才能看到视觉效果（与 [`border-style`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-style) 或 [`border-image`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-image) 有关），否则，本属性产生的样式变化会被边框覆盖。**

## 语法

```css
/* Keyword values */
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text;

/* Global values */
background-clip: inherit;
background-clip: initial;
background-clip: unset;
```

### border-box

背景延伸至边框外沿（但是在边框下层）。

### padding-box

背景延伸至内边距（[`padding`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/padding)）外沿。不会绘制到边框处

### content-box

背景被裁剪至内容区（content box）外沿。

### ==text==

背景被裁剪成文字的前景色。

## 实际效果

### border-box

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .box {
            width: 100px;
            height: 100px;
            background-color: red;
            border: 10px double yellow;
            background-clip: border-box;
        }
    </style>
</head>
<body>
<div class="box">

</div>
</body>
</html>

```

![Screenshot2022-11-28 PM9.01.20](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-28%20PM9.01.20.png)
