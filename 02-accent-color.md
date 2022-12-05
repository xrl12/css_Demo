# accent-color的使用

## 介绍

**重音颜色CSS属性设置由某些元素生成的用户界面控件的重音颜色。**

## 语法

```
accent-color = 
  auto     |
  <color>  
```

## 浏览器兼容

![image-20221205165806032](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/image-20221205165806032.png)

## 支持的元素

### input
```html
<input type="checkbox"/>
<input type="radio"/>
<input type="range"/>
```

### progress

```html
<progress></progress>
```

## 实际效果

没有添加的样式

![image-20221205165856628](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/image-20221205165856628.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>02-accent-color</title>
    <style>
        .input1 {
            accent-color: green;
        }

        .input2 {
            accent-color: grey;
        }

        .input3 {
            accent-color: antiquewhite;
        }

        progress {
            accent-color: blueviolet;
        }
    </style>
</head>
<body>
<input type="checkbox" class="input1"></input>

<input type="radio" class="input2"></input>
<input type="range" class="input3"></input>

<progress></progress>
</body>
</html>
```

![image-20221205170440146](https://golanage.oss-cn-beijing.aliyuncs.com/css_demo/image-20221205170440146.png)
