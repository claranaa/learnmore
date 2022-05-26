### 函数定义的两种方式

1. 函数表达式

   ```js
   var foo = function() {
       console.log('kk')
   }
   ```

2. 函数声明

   ```js
   function boo() {
   	console.log('rr')
   }
   ```

   

### 函数内this的指向

this的指向，是当调用函数的时候确定的。调用方式的不同决定了this的指向不同。一般指向我们的调用者。

| 调用方式     | this指向                                  |
| ------------ | ----------------------------------------- |
| 普通函数调用 | window                                    |
| 构造函数调用 | 实例对象 原型对象里面的方法也指向实例对象 |
| 对象方法调用 | 该方法所属对象                            |
| 事件绑定方法 | 绑定事件对象                              |
| 定时器函数   | window                                    |
| 立即执行函数 | window                                    |

注：（1）匿名函数也指向window（2）IE中attachEvent中的this总是指向全局对象window

### 闭包

闭包需要满足以下特征：（1）有外层函数嵌套内层函数；（2）内层函数使用外层函数的局部变量；（3）内层函数返回外部，并且被全局变量保存。



### 原型链

对象在调用方法和属性时依靠原型链的顺序进行查找，先从自身查找，然后是构造函数的原型对象，接着是Object的原型对象，一旦找到时停止查找，找不到则返回undefined。同时，原型对象中的this仍然指向实例对象，而非原型对象。



### JavaScript数据类型之原始值和引用值



|          | 原始值                                                   | 引用值                                                       |
| -------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| 位置     | 存储在栈中的简单数据段，他们的值直接存储在变量访问的位置 | 存储在堆中的对象，处处在变量出的值是一个指针，指向存储对戏那个的内存处 |
| 数据类型 | undefined、null、boolean、number、string、Symbol         | Object                                                       |

### JavaScript数据类型之转换为true/false的值

| 数据类型  | 转换为true的值               | 转换为false的值  |
| --------- | ---------------------------- | ---------------- |
| Boolean   | true                         | false            |
| String    | 任意非空字符串               | 空字符串         |
| Number    | 任意非零数字值（包括无穷大） | 0和Null,NaN==NaN |
| Object    | 任意对象                     |                  |
| null      | null==undefined              | null             |
| Undefined |                              | Undefined        |



### Ajax与Flash的优缺点

|       | 优点                                         | 缺点                                                         |
| ----- | -------------------------------------------- | ------------------------------------------------------------ |
| Ajax  | 可搜索性、可开放性、易用性、易于开发         | 它可能破坏浏览器的后退功能；使用动态页面更新使得用户难于将某个特定的状态保存到收藏夹中 |
| Flash | 多媒体处理、兼容性、矢量图形、客户端资源调度 | 二进制格式；格式私有；flash文件经常会很大，用户第一次使用的时候需要忍耐较长的等待时间；性能问题 |



### 数组的API

arr.filter()用于筛选出满足要求的数组元素，并返回新的数组。

arr.some()用于检测数组是否有满足条件的元素，只要存在元素满足要求，则返回flase。

arr.every()用于检测数组的所有元素是否都满足条件，都满足条件时返回true，否则返回flase。

arr.map()会对数组中每个元素进行单独判断，返回true或者flase，作为新数组的元素。

对于数组 arr = [2,20,3,12,9] 

```js
var res = arr.filter((val1,val2)=>{

return val1 > 10;

})

console.log(res); // [20, 12]
```

```js
var res = arr.some((val1,val2)=>{

return val1 > 10;
})
console.log(res);  // true
```

```js
var res = arr.every((val1,val2)=>{

return val1 > 10;

})

console.log(res);  // false
```

```js
var res = arr.map((val1,val2)=>{

return val1 > 10;
})
console.log(res);  // [false, true, false, true, false]
```

### 

| 方法             | 描述                                                         |        |
| ---------------- | ------------------------------------------------------------ | ------ |
| concat()         | 连接两个或多个数组，并返回结果                               | 不改变 |
| join()           | 把数组的所有元素放入一个字符串，元素通过指定的分隔符进行分隔 |        |
| pop()            | 删除并返回数组的最后一个元素                                 | 改变   |
| reverse()        | 颠倒数组中元素的顺序                                         |        |
| shift()          | 删除并返回数组的第一个元素                                   |        |
| slice()          | 从某个已有的数组返回选定的元素                               |        |
| sort()           | 对数组的元素进行排序                                         |        |
| splice()         | 删除元素，并向数组添加新元素                                 | 改变   |
| toString()       | 把数组转换为字符串，并返回结果                               |        |
| toLocaleString() | 把数组转换为本地数组，并返回结果                             |        |
| unshift()        | 向数组的开头添加一个或更多的元素，并返回新的长度             |        |
| valueOf()        | 返回数组对象的原始值                                         |        |
|                  |                                                              |        |
|                  |                                                              |        |



### JS对象

JS对象分为三大类：内置对象、宿主对象、自定义对象

- JS中的内置对象

  | Arguments | 函数参数集合   |
  | --------- | -------------- |
  | Array     | 数组           |
  | Boolean   | 布尔对象       |
  | Date      | 日期时间       |
  | Error     | 异常对象       |
  | Function  | 函数构造器     |
  | Math      | 数学对象       |
  | Number    | 数值对象       |
  | Object    | 基础对象       |
  | RegExp    | 正则表达式对象 |
  | String    | 字符串对象     |

- 宿主对象

  运行环境提供的对象：如Window和Document，Element，form，image。

- 自定义对象

  开发人员定义的对象。

### call、apply、bind的使用

- call的写法

  ```js
  Function.call(obj,[param1[,param2[,…[,paramN]]]])
  ```

  注意：

  （1）调用 call 的对象，必须是个函数 Function。

  （2）call 的第一个参数，是一个对象。 Function 的调用者，将会指向这个对象。如果不传，则默认为全局对象 window。

  （3）第二个参数开始，可以接收任意个参数。每个参数会映射到相应位置的 Function 的参数上。但是如果将所有的参数作为数组传入，它们会作为一个整体映射到 Function 对应的第一个参数上，之后参数都为空。

  ```js
  function func (a,b,c) {}
  
  func.call(obj, 1,2,3)
  // func 接收到的参数实际上是 1,2,3
  
  func.call(obj, [1,2,3])
  // func 接收到的参数实际上是 [1,2,3],undefined,undefined
  ```

- apply的写法

  ```js
  Function.apply(obj[,argArray])
  ```

  注意：

  （1）它的调用者必须是函数 Function，并且只接收两个参数，第一个参数的规则与 call 一致。

  （2）第二个参数，必须是数组或者类数组，它们会被转换成类数组，传入 Function 中，并且会被映射到 Function 对应的参数上。这也是 call 和 apply 之间，很重要的一个区别。

  ```js
  func.apply(obj, [1,2,3])
  // func 接收到的参数实际上是 1,2,3
  
  func.apply(obj, {
      0: 1,
      1: 2,
      2: 3,
      length: 3
  })
  // func 接收到的参数实际上是 1,2,3
  ```

- bind的写法

  ```js
  Function.bind(thisArg[, arg1[, arg2[, ...]]])
  ```

  注意： bind 方法 与 apply 和 call 比较类似，也能改变函数体内的 this 指向。不同的是，**bind 方法的返回值是函数，并且需要稍后调用，才会执行**。而 apply 和 call 则是立即调用。 

  ```js
  function add (a, b) {
      return a + b;
  }
  
  function sub (a, b) {
      return a - b;
  }
  
  add.bind(sub, 5, 3); // 这时，并不会返回 8
  add.bind(sub, 5, 3)(); // 调用后，返回 8
  ```

- 总结：

  call 和 apply 的主要作用，是改变对象的执行上下文，并且是立即执行的。它们在参数上的写法略有区别。

  bind 也能改变对象的执行上下文，它与 call 和 apply 不同的是，返回值是一个函数，并且需要稍后再调用一下，才会执行。

### 不支持冒泡的事件

（1）mouseenter （2）mouseleave （3）bulr （4）load （5）unload （6）focus （7）resize

