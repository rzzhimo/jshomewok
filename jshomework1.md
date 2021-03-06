﻿# The comparation between React and Vue and my experience of learning Vue
![React and Vue cpmparation](http://p0.qhimg.com/t016ed168688ebc74f8.jpg)
---

## 1.What is React
![React](http://ww2.sinaimg.cn/large/c5131475jw1ey7e3pywnhj20ku08pmxw.jpg)
>1.**origin**:React originated as an internal project on Facebook, and because the company was unhappy with all the JavaScript MVC frameworks on the market, it decided to write its own set of Instagram sites.When it was done, it was found to be very useful, and it was opened in May 2013.

>2.From the earliest UI engine to a whole set of front-end
**Web App solutions**.The reaction Native project spawned is even more ambitious, and we hope to write Native apps in the way of writing Web apps.

>3.React is mostly used to build **UI**.You can pass multiple types of parameters in the React, such as declaration code to help you render the UI, static HTML DOM elements, dynamic variables, and even interactive application components.

---
### 1)React 's characteristic
>1. **Declarative design**: the React USES a declarative paradigm to describe applications easily.

>2. **Efficient**: the React minimizes interaction with the DOM by simulating it.

>3. **Flexibility**: the React can work well with known libraries or frameworks.

---
## 2.What is Vue
![React](http://img.mp.itc.cn/upload/20170715/663e057ce42c419e9eeeb126570585ae_th.jpg)
>1.Vue is an **incremental framework** for building user interfaces.Unlike other large frameworks, Vue is designed to be applied layer by layer from bottom to top.

>2.Vue's core library focuses only on the **view layer**, making it easy to get started and integrate with third-party libraries or existing projects.

>3.On the other hand, when combined with modern toolchains and various supporting libraries, Vue is perfectly capable of providing drivers for **complex single-page applications**.

---
### 1)Vue's characteristic

> 1.Lightweight framework
> 2. Two-way data binding
> 3. The instruction
> 4. Pluggable

----
### Vue'sAdvantages include:
> * Elastic selection of templates and rendering functions
> * Simple syntax and project creation
> * Faster rendering speed and smaller size

### React'sAdvantages include:
> * Better for large applications and better testability
> * It applies to both Web and native apps
> * Larger ecosystems bring more support and tools

---
### Most of their best features are the same:
> * Fast rendering using virtual DOM
> * lightweight
> * Responsive component
> * Server-side rendering
> * Easy to integrate routing tools, packaging tools, and 
> * status management tools
> * Excellent support and community

---
## 3.My experiences of learning Vue
---
### 1).the example:
``` html
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>Vue 测试实例 - 菜鸟教程(runoob.com)</title>
	<script src="https://cdn.bootcss.com/vue/2.4.2/vue.min.js"></script>
</head>
<body>
    <div id="vue_det">
        <h1>site : {{site}}</h1>
        <h1>url : {{url}}</h1>
        <h1>Alexa : {{alexa}}</h1>
    </div>
    <script type="text/javascript">
    // 我们的数据对象
    var data = { site: "菜鸟教程", url: "www.runoob.com", alexa: 10000}
    var vm = new Vue({
        el: '#vue_det',
        data: data
    })
    // 它们引用相同的对象！
    document.write(vm.site === data.site) // true
	document.write("<br>")
    // 设置属性也会影响到原始数据
    vm.site = "Runoob"
    document.write(data.site + "<br>") // Runoob

    // ……反之亦然
    data.alexa = 1234
    document.write(vm.alexa) // 1234
    </script>
</body>
</html>
```
>* Create Vue instance:

``` html
var vm = new Vue({
    // options

})
```

> 1. there is an **el** parameter in the Vue constructor, which is the id in the DOM element.All changes are within the div specified above, and the div external is not affected.

> 2. **Data** is used to define properties.
**Methods** is used to define a function that returns its     value through return.
**{{}}}** is used to output object properties and function    return values.
> 3. When a Vue **instance** is created, it adds all the attributes found in its data object to Vue's responsive system.When the values of these attributes change, the HTML view changes accordingly.
> 4. In addition to data attributes, Vue instances provide some useful instance attributes and methods.They all have the **prefix $** to distinguish them from user-defined attributes.

----
### 2). vue.js'Template syntax

>* Vue.js uses an HTML based template syntax that allows developers to bind **DOM** declaratively to the **data** of the underlying Vue instance.
>* At the heart of vue.js is a system that allows you to declaratively render data into the DOM using concise template syntax.
>* Combined with the response system, Vue can intelligently calculate the minimum cost of rerendering components and apply it to DOM operations when the application state changes.

#### example: Use the v-html instruction to output the HTML code:
``` html
<div id="app">
    <div v-html="message"></div>
</div>
    
<script>
new Vue({
  el: '#app',
  data: {
    message: '<h1>菜鸟教程</h1>'
  }
})
</script>
```
### 3).vue.js's Loop statement
>* Loop through the **v-for** instruction.
>* The v-for instruction requires a special syntax in the form of **site in sites**, an array of source data and an alias for an array element iteration.
>* V-for can bind data to an array to render a list:

#### example:
``` html
<div id="app">
  <ol>
    <li v-for="site in sites">
      {{ site.name }}
    </li>
  </ol>
</div>
 
<script>
new Vue({
  el: '#app',
  data: {
    sites: [
      { name: 'Runoob' },
      { name: 'Google' },
      { name: 'Taobao' }
    ]
  }
})
</script>
```
### 4).vue.js's Calculate attribute
>* Computed attribute keyword: computed.
>* Calculating attributes is useful when dealing with some complex logic.
``` html
<div id="app">
  {{ message.split('').reverse().join('') }}
</div>
```
>* We can use **methods** instead of computed, and the effect is the same, but computed is based on its dependency **cache** and revalues only if the dependent **dependencies** change.Using methods, the function always calls execution again when **rendering**.

## 4.Summary
> Vue is a good tool that gives us an opportunity to learn more about the framework. The **framework** is well used and skillful. When we are no longer satisfied with the surface, we can learn more about it.For example, how does vue implement **data binding**, how does it implement deeper technical principles such as **data response**.That makes a lot of sense
