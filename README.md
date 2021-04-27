# FE Interview

这里会记录找工作以及学习期间的一些面试题。

[面试日程](./面试日程.md)

## 技术向

### 计算机基础

### http

- http 状态码 301 和 302 的区别
- **说说 http 缓存，强缓存和协商缓存的区别？（🌟🌟🌟🌟🌟）**
- http1.x 和 http2.x 的区别？

### 浏览器基础

- **描述一下浏览器从输入一个URL到页面渲染的过程**
- 说说重绘和回流
- requestAnimationFrame 的执行机制是什么？

### JavaScript 基础

- JS 有哪些数据类型？
- parseInt() 和 Number() 的区别
- 如何写一个会过期的localStorage，说说想法
- 请你说说scrollIntoView的兼容性和参数
- **[深拷贝和浅拷贝的区别](./深拷贝和浅拷贝的区别)**，[如何实现一个深拷贝](https://www.cnblogs.com/wangyong1997/p/13577725.html)？
- 如何判断数据类型？Object.prototype.toString.call(data)
- setTimeout 和 setInterval 的区别
- 说说原型链
- 什么是作用域？说一下对作用域链的理解？
- js的constructor和别的语言的constructor有什么不一样？
- 如何实现一个 Promise?（代码题）
- 如何交换两个变量的值？（代码题）
- [说一下 JS 事件循环？](https://www.jianshu.com/p/184988903562)
- [说一下事件捕获和事件冒泡？](https://zhuanlan.zhihu.com/p/100831300)
- 实现跨域有哪些方案？
- cookie 的作用？我们还需要 cookie 吗？它有什么优缺点？
- 如何复制一个对象？
- web worker 是什么？它的应用？
- 闭包是什么？如何实现一个闭包？项目中的应用场景？
- 为什么 0.1 +. 0.2 !== 0.3？
- **事件委托（代理）？**

#### ES6

-  **ES6有哪些新特性？**
- 箭头函数的 this 指向?
- 箭头函数和普通函数的区别？
- Proxy 是什么？它和 Object.defineProperty 的区别?
- 了解过 Promise/A+ 规范吗？
- 如何实现一个Promise方法?
- var 和 const / let 的区别
- 了解过 Promise/A+ 规范吗？
- 解构和普通赋值操作的区别？解构的原理？
- 讲讲 js 中的原型链？`__proto__` 和 `prototype` 有什么区别？分别是做什么的？
- promise 和 async/await 的区别？
- ES6 class 和普通 function 创建构造函数的区别？

### TypeScript

- 项目中有使用过 TypeScript 吗？

### 框架相关

#### 框架关系/比较

- 对比React和Vue
- 对比jsx和template
- 对比hooks和composition
- 虚拟dom在React和Vue中的区别
- redux 和 vuex 的区别
- redux 如何实现异步？
- 对比一下 uniapp 和 taro?
- react 和 vue 的生命周期如何对应？

#### 虚拟DOM

- 什么是虚拟DOM？
- 为什么需要使用虚拟DOM?
- 虚拟DOM的工作原理？

#### React

- class组件和es6的class的关系？
- class中constructor的为什么需要super(props)
- 对jsx的理解？React17的jsx发生了什么变化？
- 高阶组件？
- 对hooks的理解？
- hooks函数组件和class组件的区别？分别都有什么优缺点？
- fiber架构？
- 长虚拟列表设计方案
- [React 中的合成事件有了解过吗？](https://www.dazhuanlan.com/2020/03/23/5e7874ae23149/)
- react 中 setState 是同步还是异步的？流程是怎样的？如果在 setTimeout 当中执行 setState 是同步还是异步的？为什么？
- 如何在 useEffect 中调用 async 函数？

#### Vue

- this.nextTick怎么理解？
- Vue3 的新特性有没有了解过？
- keep-alive 的作用？涉及到哪些钩子？需要配合什么来实现？
- vue 中 v-model 的原理？
- vue 中修改一个 state，它如何将状态改变映射到 template 中？

### Taro

- Taro2.x 和 3.x 版本的区别？
- Taro3 如何实现不同框架适配多端？

### 状态管理

- 什么情况下需要用到状态管理？
- Redux 的原理是什么？

### 构建工具 / 模块化

- webpack  和 rollup 的区别
- 有没有手写过 webpack loader? loader 的执行原理是什么？
- rollup 可以打包成哪些规范的产物？分别适用于什么？
- CommonJS 和 ESModule 的区别？import 和 require 的区别？
- 了解过 webpack tree-shaking 吗？如何配置？它的原理是什么？
- 用过哪些 webpack 的配置？

### 性能优化

- 常用的性能优化手段(webpack/React/Vue/Css/缓存)
- 长列表优化方案
- 首屏加载如何优化？DEVTool 中相关的一些参数/属性？

### 设计模式

- 观察者模式
- 发布/订阅模式
- 说说在项目中常用到的一些算法和设计模式？

### 架构

- 说说从 uniapp 到 taro 的重构中，你都做了哪些工作？
- 项目搭建如何考虑？
- 看你写了组件库的封装，说说在组件库封装过程中需要注意的点
- 项目中的 axios 请求类怎么封装？

### 未分类

- 前端引起内存泄漏的常见原因
- 多列瀑布流列表设计方案
- 说说你对Web Components的理解(对比React/Vue组件)
- 说说你对shadow DOM的理解
- 请你说说让不同的浏览器兼容ES6的方法
- 项目中 axios 如何封装？
- go 语言有没有了解过？

### CSS

- grid 布局有用到过吗？
- 有用过 flex 吗？说说它有哪些常用的属性？
- 了解过 BFC 吗？如何实现一个 BFC？它的用途是什么？
- margin 层叠了解过吗？
- 如何实现一个元素水平居中？

### Web 安全

- 说说 XSS 攻击？如何预防？

## 非技术向

- 说说你日常生活中的爱好
- 请介绍一下你有哪些特长呢？
- 请问你的工作经历有哪些呢？
- 用三个词来形容自己？
- 说说自己的优点？还有自己的不足呢？
- 工作三年多来，你遇到过最大的挑战是什么？你觉得成长最大的是哪一个阶段？






