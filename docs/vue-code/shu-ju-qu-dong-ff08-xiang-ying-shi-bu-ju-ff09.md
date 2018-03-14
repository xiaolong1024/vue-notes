官方：[Vue 最独特的特性之一，是其非侵入性的响应式系统。数据模型仅仅是普通的 JavaScript 对象。而当你修改它们时，视图会进行更新。](https://cn.vuejs.org/v2/guide/reactivity.html)![](/image/xiangying.png)从上图中和官方的说明  vue是使用[Object.defineProperty](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)把这些属性全部转为 getter/setter 来实现响应式。

#### **Object.defineProperty**

直接在一个对象上定义一个新属性，或者修改一个已经存在的属性， 并返回这个对象。

Object.defineProperty\(obj, prop, descriptor\)

* `obj`需要定义属性的对象。
* `prop`需被定义或修改的属性名。
* `descriptor`需被定义或修改的属性的描述符。 



