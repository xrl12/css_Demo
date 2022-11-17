# linear-gradient的使用

## 介绍

CSS **`linear-gradient()`** 函数用于创建一个表示两种或多种颜色线性渐变的图片。其结果属于[`<gradient>`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/gradient)数据类型，是一种特别的[`<image>`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/image)数据类型

## 语法

```css
linear-gradient(
  [ <angle> | to <side-or-corner> ,]? <color-stop-list> )
  \---------------------------------/ \----------------------------/
    Definition of the gradient line        List of color stops

where <side-or-corner> = [ left | right ] || [ top | bottom ]
  and <color-stop-list> = [ <linear-color-stop> [, <color-hint>? ]? ]#, <linear-color-stop>
  and <linear-color-stop> = <color> [ <color-stop-length> ]?
  and <color-stop-length> = [ <percentage> | <length> ]{1,2}
  and <color-hint> = [ <percentage> | <length> ]
```

### angle

用角度值指定渐变的方向（或角度）。角度顺时针增加。

### side-or-corner

描述渐变线的起始点位置。它包含 to 和两个关键词：第一个指出水平位置 left or right，第二个指出垂直位置 top or bottom。关键词的先后顺序无影响，且都是可选的。 to top, to bottom, to left 和 to right 这些值会被转换成角度 0 度、180 度、270 度和 90 度。其余值会被转换为一个以向顶部中央方向为起点顺时针旋转的角度。渐变线的结束点与其起点中心对称。

### linear-color-step

由一个[`<color>`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color_value)值组成，并且跟随着一个可选的终点位置（可以是一个百分比值或者是沿着渐变轴的[`<length>`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/length)）。CSS 渐变的颜色渲染采取了与 SVG 相同的规则。

### color-hint

颜色中转点是一个插值提示，它定义了在相邻颜色之间渐变如何进行。长度定义了在两种颜色之间的哪个点停止渐变颜色应该达到颜色过渡的中点。如果省略，颜色转换的中点是两个颜色停止之间的中点。

## 实际效果

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body,
        html {
            margin: 0;
            padding: 0;
        }

        .box {
            width: 500px;
            height: 500px;
            background: linear-gradient(#d70a1a, #008);
          	/* 从d70a1a到#008过渡 */
        }
    </style>
</head>
<body>
<div class="box"></div>
</body>
</html>

```

![Screenshot2022-11-17 PM8.46.33](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-17%20PM8.46.33.png)`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body,
        html {
            margin: 0;
            padding: 0;
        }

        .container > div {
            margin-bottom: 200px;
            width: 500px;
            height: 500px;
        }

        .box2 {
            background: linear-gradient(to left, red, yellow, orange);
          	/* 从左到右 从红色到黄色到橙色过渡 */
        }
    </style>
</head>
<body>
<div class="container">
    <div class="box2"></div>
</div>

</body>
</html>

```

![Screenshot2022-11-17 PM8.52.47](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-17%20PM8.52.47.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body,
        html {
            margin: 0;
            padding: 0;
        }

        .container > div {
            margin-bottom: 200px;
            width: 500px;
            height: 500px;
        }

        .box3 {
            background: linear-gradient(to right, black, orange, gray);
            /* 从右到左，从黑色到橙色到灰色过渡 */
        }
    </style>
</head>
<body>
<div class="container">
    <div class="box3"></div>
</div>

</body>
</html>

```

![Screenshot2022-11-17 PM8.55.38](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-17%20PM8.55.38.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body,
        html {
            margin: 0;
            padding: 0;
        }

        .container > div {
            margin-bottom: 200px;
            width: 500px;
            height: 500px;
        }
      
        .box4 {
            background: linear-gradient(45deg, blue, #d90000);
            /* 45度倾斜 从蓝色到#d90000过渡  */
        }
    </style>
</head>
<body>
<div class="container">
    <div class="box4"></div>
</div>

</body>
</html>

```

![Screenshot2022-11-17 PM8.59.48](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-17%20PM8.59.48.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body,
        html {
            margin: 0;
            padding: 0;
        }

        .container > div {
            margin-bottom: 200px;
            width: 500px;
            height: 500px;
        }
      
        .box5 {
            background: linear-gradient(90deg, red 10%, yellow 30%, green 50%, blue 80%);
          /* 90度倾斜，从从红色开始渐变  从%5开始渐变，从20%开始渐变到黄色，从50开始渐变绿色，从80开始渐变蓝色 */
        }
    </style>
</head>
<body>
<div class="container">

    <div class="box5"></div>
</div>

</body>
</html>

```



![Screenshot2022-11-17 PM9.05.20](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/Screenshot2022-11-17%20PM9.05.20.png)
