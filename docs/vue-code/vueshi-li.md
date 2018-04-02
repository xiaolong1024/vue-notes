![](/image/shengming.png)

el属性传入的如果不是element，最后会通过`document.querySelector`来获取的，这个接口性能较差，所以，el传入一个element性能会更好。

* `$mount`方法中对`html`，`body`标签做了过滤，这两个不能用来作为渲染的根节点。

* 每一个组件都会从`_init`开始重新运行，所以，当存在一个长列表时，将子节点作为一个组件，性能会较差。

* `*.vue`文件会在构建时转化为`render`方法，而`render`方法的性能比指定`template`更好。所以，源码使用`*.vue`的方式，性能更好。

* 如果需要自定义`delimiters`，每一个组件都需要单独指定。

* 如果是`*.vue`文件，指定`delimiters`是失效的，因为`vue-loader`对`*.vue`文件进行解析时，并没有将`delimiters`传递到`compiler.compile()`中。（这一点不确定是bug还是故意这样设计的）。

#### 怎样找到入口函数

##### 1.全局搜索？

##### 2.百度 google

##### 3.vue项目 node项目

1. package.json ![](/image/package.png) 
2. config.js![](/image/scripts_config.png)
3. entry-runtime-with-compiler.js![](/image/entry-runtime-with-compiler.png)
4. runtime/index.js![](/image/runtime_index.png)
5. core/index.js![](/image/core_index.png)
6. core/instance/index.js![](/image/core_instance_index.png)

#### **vue构造函数**

**vue/src/core/instance/index.js**![](/image/instance/index.png)

#### 初始化函数

**vue/src/core/instance/init.js**![](/image/instance/init.png)

