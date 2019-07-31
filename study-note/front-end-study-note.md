> 作为一个在后端领域摸爬打滚了几年的人来说，入门前端应该是不难的，毕竟语言的语法可能不同，但是有些思想却是一样的，要想形成一个长久的记忆，知识体系的构建是相当重要的。

* HTML+CSS+JavaScript

```
    这三件法宝可以说是前端不变的基石了，不管前端的框架如何繁多，变化频率如何快，底层肯定都是基于这三者的，因为浏览器的就是解析这三者的(浏览器有实现标准，这些标准需要参考这三大基石，而不是React，VUE啥的)，所以不要把各种框架想的有多复杂，底层肯定就是简单的HTML，CSS，JavaScript。毕竟复杂也是从简单开始，生命的起源就是在大海里，从单细胞生物开始，慢慢才有了多细胞生物，再到有着复杂系统的生物，这就是进化，进化基于简单开始。前端的交互再如何复杂绚丽，最终还是回归到了静态页面上面，也就是HTML+CSS+JavaScript。
```

```
这方面的学习和后续查找资料推荐MDN，mozilla可是浏览器的鼻祖，它的技术文档还是比较靠谱,权威,全面
学习网站:
https://developer.mozilla.org/zh-CN/
```

* HTML

```
学习网站(MDN):
https://developer.mozilla.org/zh-CN/docs/Web/HTML
```

```
element的分类及特点，三大类?
块级元素：独占一行；高度和宽度通过属性设置决定（div，ul）
内联元素：多个同类型标签同时显示在一行；高度和宽度由内容决定（span）
块级-内联：多个同类型标签显示在一行；高度和宽度通过属性设置决定（button，input）
tips:这些特性只是它们原生的特点，如果真的需要，可以通过属性设置来改变它们原生的特点达到相互转换的目的
```



* CSS

```
学习网站(MDN):
https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS
```

```
CSS的作用是更改网页内容的字体，颜色，大小和间距。
```

```
CSS如何工作的？
https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works
了解这点很重要，比知道语法更重要!!!看MDN画的那副图，巨准确。

1.浏览器加载HTML文件
2.浏览器解析HTML文件中的内容
3.HTML文件中会有对CSS的引用，浏览器于是开始加载CSS文件。
4.浏览器解析HTML中的内容并构建DOM树
5.浏览器解析CSS并把它结合到DOM内容中
6.浏览器显示整个文档
```

```
CSS如何应用到HTML上？
三种方式:
1.外部样式表(推荐使用)：
HTML文件:
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>

CSS文件:
h1 {
  color: blue;
  background-color: yellow;
  border: 1px solid black;
}

p {
  color: red;
}

2.内部样式表:
当不能不能直接修改CSS文件时,可以使用

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
    <style>
      h1 {
        color: blue;
        background-color: yellow;
        border: 1px solid black;
      }

      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first CSS example</p>
  </body>
</html>


3.内联样式(不推荐使用):
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My CSS experiment</title>
  </head>
  <body>
    <h1 style="color: blue;background-color: yellow;border: 1px solid black;">Hello World!</h1>
    <p style="color:red;">This is my first CSS example</p>
  </body>
</html>
```

```
CSS规则？
由两部分组成：
属性(property)：比如字体颜色，字体大小
属性值(value)：属性对应的值
```

```
CSS选择器(selector)有哪些?
https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Selectors

简单选择器:
属性选择器:
伪类和伪元素:
组合器和多用选择器:
```

```
CSS的层叠规则?
https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance

层叠意味着有可能某部分的样式重叠了，比如有的规则让这部分内容的字体变为红色，有的规则让它变为蓝色，这两个规则重叠了，优先级如何决定?
```

* JavaScript

```
学习网站(MDN)
https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript
```

```
我们看到网站页面有动态效果，其实这就是js的功劳，它可以通过接口来动态改变HTML和CSS达到动态的目的。它是用户端(User-Agent,一般指的就是浏览器)。所以动态的指的是HTML或者CSS变了。
```



