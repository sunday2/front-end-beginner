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
    我们看到网站页面有动态效果，其实这就是JavaScript的功劳，它可以通过动态改变HTML和CSS达到动态的目的。它是用户端(User-Agent,一般指的就是浏览器)脚本语言。所谓动态的指的是HTML或者CSS变了。JavaScript是解释型语言。
```

```
    既然是用户端脚本语言，肯定有它的运行环境，浏览器的实现确实内嵌了JavaScript引擎，用来执行js。而为了使js能够脱离浏览器执行，就有了node.js(基于chrome的第八代js引擎开发)，有了它，js能够脱离浏览器，基于node.js而运行。所以主流的前端框架，如果想在本地运行，都是要配置js的运行环境node.js。也因为有了node.js，js甚至可以运用在后端，作为后端脚本语言(js既然作为客户端语言也能作为后端语言)。
```

```
JavaScript为什么能够实现交互？
https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript

JavaScript能够实现交互或者说动态的原因在于API。API又分为了两大种。
1.浏览器API：
内建于浏览器中(所以可能a浏览器支持api，b浏览器不支持该api)，它们可以使周边计算环境的数据暴露出来。
包括：
(1)文档对象模型API。能通过创建，移除和修改HTML，为页面动态应用新样式等手段来操作 HTML 和 CSS。
(2)地理位置API。获取地理信息，这就是为什么谷歌地图可以找到你的位置。
(3)画布(Canvas)和WebGL API 创建2D 和3D图像。
(4)影像类API。

2.第三方API：
这类API未嵌入浏览器中，一般从网上取得它们的信息。包括：
(1)Twitter API和新浪微博API
(2)谷歌地图API和高德地图API可以在网站嵌入定制的地图。
(3)平时我们说的前后端交互其实也是理解为第三方接口。

```

```
JavaScript在浏览器上作了什么?
https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript

在 HTML 和 CSS 集合组装成一个网页后，浏览器的 JavaScript 引擎将执行 JavaScript 代码。这保证了当 JavaScript 开始运行之前，网页的结构和样式已经就位。
这样很好，因为通过 DOM API（见上文）动态修改 HTML 和 CSS 来更新 UI 正是 JavaScript 最普遍的用处所在。如果 JavaScript 在 HTML 和 CSS 就位之前加载运行，就会引发错误。
```

```
JavaScript执行顺序？

为了防止控制台出现undefined问题，我们需要注意js脚本定义的出现顺序。
```

```
如何向页面添加JavaScript?
https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript

(1)内部JavaScript
在HTML文件中的 </body> 标签结束前插入以下代码：
<script>
  // 在此编写 JavaScript 代码
</script>

(2)外部JavaScript(推荐)
在HTML中<head>标签中嵌入外部的js文件。
<script src="script.js" async></script>


(3)内联JavaScript处理器(强烈不推荐)
<button onclick="createParagraph()">点我呀</button>

这将使 JavaScript 污染到 HTML，而且效率低下。对于每个需要应用 JavaScript 的按钮，你都得手动添加 onclick="createParagraph()" 属性。
可以使用纯 JavaScript 结构来通过一个指令选取所有按钮。

```

```
JavaScrpt脚本调用顺序策略?（非常重要）
https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript#%E5%86%85%E8%81%94_JavaScript_%E5%A4%84%E7%90%86%E5%99%A8

(1)如果脚本无需等待页面解析，且无依赖独立运行，那么应使用 async。
(2)如果脚本需要等待解析，且依赖于其它脚本，调用这些脚本时应使用 defer，将关联的脚本按所需顺序置于 HTML 中。
```

* React
```
React官方中文教程
https://zh-hans.reactjs.org/docs/components-and-props.html
实战教程:
https://zh-hans.reactjs.org/tutorial/tutorial.html
```

```
目前主流三大前端框架之一，在三大框架的使用率上，2019年目前仍然是React的使用率最高(大幅领先)，Angular次之，VUE次之。
通过npm trends网站可以知道三者下载量的一个趋势:
https://www.npmtrends.com/angular-vs-react-vs-vue
```

```
React的入门我觉得官方的教程挺好，直接动手实践是最快成长的方式，官方的教程也写的很好。
```
```
React是一个声明式，高效且灵活的用于构建用户界面的JavaScript库。
```

```
环境准备(本地开发):
1.安装Node.js(JavaScript运行环境，基于chrome V8 js引擎开发)。
由于JavaScript的运行需要对应的js引擎(浏览器本身内嵌有js引擎)，所以如果脱离浏览器在本地运行的话肯定得有JavaScript的运行环境--Node.js。这个步骤就类似java需要安装jdk一样。
2.安装npm。npm是JavaScript语言的一个包管理工具。这个就类似java中的maven。
```

```
React中的组件?
使用React可以将一些简短的，独立的代码片段组合成更复杂的UI界面，这些代码片段就是组件。

React原生已经提供了很多不同类型的组件，如果需要自定义组件，可以通过extends React.Component子类开始。
```
```
如何定义一个组件？
```


```
如何在a组件中使用b组件?
```

```
参数如何在组件中传递?

每个组件最终返回的是一个html片段，也就是element。element有属性(K-V键值对)，也就是property。组件内部通过
this.props.property
就可以获取对应的属性值了。


并且函数也可以进行传递！！！！
```

```
如何引用变量?
{variable}
```

```
组件中构造函数的使用?

组件就类似java中的类，当然，class在js中只是个语法糖。那么类或者说组件可以定义自己内部的一些状态或者说变量或者说对象。

//构造函数名和参数固定写法
constructor(props){
	  //调用父构造函数,固定写法
      super(props);
      //定义组件内部自己的状态，这里state是一个json对象
      this.state = {
        value:null,
      };
}

```

```
在浏览器安装React Devtools插件方便点击右键选择"查看"直接打开开发者工具。
```

```
给element绑定监听事件函数要注意的地方?

注意：此处使用了 onClick={() => alert('click')} 的方式向 onClick 这个 prop 传入一个函数。 React 将在单击时调用此函数。但很多人经常忘记编写 () =>，而写成了 onClick={alert('click')}，这种常见的错误会导致每次这个组件渲染的时候都会触发弹出框。
```

```
如何进行前后端交互?

```

```
构造函数什么情况下使用？

构造函数在需要定义组件内部的私有变量时使用。
```

```
为什么不可变性在React中非常重要?

先说说两种改变数据的方式?
(1)直接在原有数据上直接修改。
var player = {score: 1, name: 'Jeff'};
player.score = 2;
// player 修改后的值为 {score: 2, name: 'Jeff'}

(2)新数据替换旧数据
var player = {score: 1, name: 'Jeff'};

var newPlayer = Object.assign({}, player, {score: 2});
// player 的值没有改变, 但是 newPlayer 的值是 {score: 2, name: 'Jeff'}

// 使用对象展开语法，就可以写成：
// var newPlayer = {...player, score: 2};

不直接修改(或改变底层数据)和直接修改的方式结果是一样的，但是拥有更多好处:
(1)简化复杂功能。可追溯数据的变化，毕竟撤销和恢复功能在开发中是一个很常见的需求。它使得复杂的特性更容易实现
(2)跟踪数据变化。如果发现对象变成了一个新对象，那么我们就可以说对象发生了改变。
(3)确定在React中何时渲染(利于进行性能优化)。不可变性最主要优势在于帮助我们在React中创建pure components。我们可以很轻松的确定不可变数据是否发生了改变，从而确定何时对组件进行重新渲染。
```

```
组件的两种定义方式?
(1)extends React.Component。
(2)函数组件。如果需要实现的组件只包含render方法，不需要私有的state，那么使用函数组件更简单。
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}。
使用函数组件时候,注意事件的绑定机制写法也不一样。
```


```
当 React 元素为用户自定义组件时，它会将 JSX 所接收的属性（attributes）转换为单个对象传递给组件，这个对象被称之为 “props”。
```
```
props如何命名？

我们建议从组件自身的角度命名 props，而不是依赖于调用组件的上下文命名。
```

```
props的只读性?

所有 React 组件都必须像纯函数一样保护它们的 props 不被更改。
tips:也就是组件传入的参数不允许在组件内部修改。
```

```
每次组件更新时 render 方法都会被调用
```

```
尽管 this.props 和 this.state 是 React 本身设置的，且都拥有特殊的含义，但是其实你可以向 class 中随意添加不参与数据流（比如计时器 ID）的额外字段。
```

```
React组件中的一些内置的生命周期方法？

(1)挂载方发。组件生命周期中的挂载方法，组件第一次渲染到DOM中的时候调用。
  
   componentDidMount() {
   }
  
  
  
2）卸载方法。组件被删除的时候调用
  componentWillUnmount() {

  }
```

```
React中即时每次都会创建新的React DOM，但是只会更新变化的element！！！！牛逼
```

```
关于React组件中state?

(1)组件的构造函数是唯一可以给this.state直接赋值的地方！！！,
this.state.comment = 'Hello';
在其余地方更新state只能通过setState方法,否则无法触动render方法重新渲染组件
this.setState({comment: 'Hello'});

(2)state的更新可能是异步的。
出于性能考虑，React 可能会把多个 setState() 调用合并成一个调用。
因为 this.props 和 this.state 可能会异步更新，所以你不要依赖他们的值来更新下一个状态。

// Wrong
this.setState({
  counter: this.state.counter + this.props.increment,
});
要解决这个问题，可以让 setState() 接收一个函数而不是一个对象。
(3)state的更新会被合并(浅合并)。	
调用 setState() 的时候，React 会把你提供的对象合并到当前的 state。

```

```
React中的数据(state)是向下流动的！！！

不管是父组件或是子组件都无法知道某个组件是有状态的还是无状态的。这就是为什么称 state 为局部的或是封装的的原因。除了拥有并设置了它的组件，其他组件都无法访问。

组件可以选择把它的 state 作为 props 向下传递到它的子组件中：

<h2>It is {this.state.date.toLocaleTimeString()}.</h2>
这对于自定义组件同样适用：

<FormattedDate date={this.state.date} />
FormattedDate 组件会在其 props 中接收参数 date，但是组件本身无法知道它是来自于 Clock 的 state，或是 Clock 的 props，还是手动输入的：

function FormattedDate(props) {
  return <h2>It is {props.date.toLocaleTimeString()}.</h2>;
}
在 CodePen 上尝试

这通常会被叫做“自上而下”或是“单向”的数据流。任何的 state 总是所属于特定的组件，而且从该 state 派生的任何数据或 UI 只能影响树中“低于”它们的组件。

如果你把一个以组件构成的树想象成一个 props 的数据瀑布的话，那么每一个组件的 state 就像是在任意一点上给瀑布增加额外的水源，但是它只能向下流动。

为了证明每个组件都是真正独立的，我们可以创建一个渲染三个 Clock 的 App 组件：

function App() {
  return (
    <div>
      <Clock />
      <Clock />
      <Clock />
    </div>
  );
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
在 CodePen 上尝试

每个 Clock 组件都会单独设置它自己的计时器并且更新它。

在 React 应用中，组件是有状态组件还是无状态组件属于组件实现的细节，它可能会随着时间的推移而改变。你可以在有状态的组件中使用无状态的组件，反之亦然。

组件可以选择把它的 state 作为 props 向下传递到它的子组件中。(所谓的向下流动)
```

```
export statement的使用？

在HTML,CSS,JS中JS是最复杂的。JS中的statement中觉得有必要重点了解下import statement，但是说到import statement得先说下export statement。
```





