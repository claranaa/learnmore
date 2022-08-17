### JS原型

#### prototype的定义

只有函数才有prototype属性，当创建函数时，JS会为这个函数自动添加prototype属性，prototype是给其它对象提供共享属性和方法的对象。



#### __ proto __的作用

首先，__ proto __ 是对象所独有的， 当你在访问一个对象属性时，如果该对象内部不存在这个属性，那么就会去它的__ proto __ 属性所指向的对象（父类对象）上查找，如果父类对象依旧不存在这个属性，那么就会去其父类的 __ proto __ 属性所指向的对象上去查找，以此类推，直到找到null。这个查找的过程，就构成了原型链。



---------------------------------------------

对象的__ proto __ 指向自己构造函数的prototype，原型链由此产生：

在创建构造函数的实例时，实例继承了构造函数上prototype的所有属性和方法（实例通过设置自己的__ proto __ 指向构造函数的prototype来实现这种继承）



原型链的尽头是Object.prototype，所有对象均从Object.prototype继承属性。



-------------------------------------------------

总结：先有Object.prototype（原型链顶端），Function.prototype继承Object.prototype而产生，最后，Function和Object和其他构造函数继承Function.prototype而产生。



Object.__ proto __ = Function.prototype

Function.__ proto __ = Function.prototype

Function.prototype.__ proto __ = Object.prototype

Object.prototype.__ proto __ = null



### 闭包

**闭包指有权访问另一个函数作用域中变量的函数。---JS高级程序设计**

闭包是一个可以访问到外部作用域的内部函数。

- 内部函数可以访问外部函数中定义的变量
- 内部函数可以访问外部函数中定义的形参
- 内部函数可以访问外部块中定义的变量

闭包需要满足以下特征：（1）有外层函数嵌套内层函数；（2）内层函数使用外层函数的局部变量；（3）内层函数返回外部，并且被全局变量保存。

#### 作用

延伸了变量的作用范围。

#### 执行上下文

当前代码执行的一个环境与范围。

#### 词法作用域

词法作用域是指内部函数在定义的时候就决定了其外部作用域。

```js
(function autorun(){
    let x = 1;
    function log(){  // 闭包的外部作用域是在其定义的时候已决定
      console.log(x);
    };
    
    function run(fn){
      let x = 100;
      fn();   // 而不是执行的时候
    }
    
    run(log); //1
})();
```

上述例子中，log( ) 函数是一个闭包，它在这里访问的是autorun()函数中的x变量，而不是run函数中的变量。autorun()的函数作用域即是log()函数的词法作用域。

#### 作用域链

每一个作用域链都有对其父作用域的引用。当使用一个变量的时候，JS引擎会通过变量名在当前作用域查找，若没有找到，会一直沿着作用域链一直向上查找，直到global全局作用域。

#### 总结

当一个函数被创建并从另一个函数返回时，它会携带一个背包，背包中是函数声明时作用域内的所有变量。

--------------------------------

被闭包引用的外部作用域中的变量将一直存活直到闭包函数被销毁。如果一个变量被多个闭包所引用，那么直到所有的闭包被垃圾回收后，该变量才会被销毁。

-------------------------------

闭包使得timer定时器，事件处理，Ajax请求等异步任务更加容易。



### this指向

this的指向，是在函数被调用的时候确定的，完全取决于函数的调用方式。

#### 普通函数调用模式

非严格模式中，普通函数中的this指向为全局对象window。

严格模式中，普通函数中的this表现为undefined。

#### 对象中的方法调用模式

指向对象本身。

#### call、apply、bind调用模式

严格模式下，绑定到指定的第一个参数。

#### 箭头函数

箭头函数的this是在创建它时外层this的指向（根据当前的词法作用域来决定this）。

- 创建箭头函数时，就已经确定了它的this指向。
- 箭头函数内的this指向外层的this。

#### new

当使用new关键字调用函数时，函数中的this一定是JS创建的新对象(实例对象)。



--------------------------------------

| 调用方式     | this指向                                  |
| ------------ | ----------------------------------------- |
| 普通函数调用 | window                                    |
| 构造函数调用 | 实例对象 原型对象里面的方法也指向实例对象 |
| 对象方法调用 | 该方法所属对象                            |
| 事件绑定方法 | 绑定事件对象                              |
| 定时器函数   | window                                    |
| 立即执行函数 | window                                    |

注：（1）匿名函数也指向window（2）IE中attachEvent中的this总是指向全局对象window



### ES6新特性

#### Promise

Promise是异步编程的一种解决方案，用来解决两个问题：

（1）回调地狱，代码难以维护。

（2）Promise可以支持多个并发的请求，获取并发请求中的数据。

注意：Promise可以解决异步的问题，但是不能说Promise本身是异步的。

--------------

Promise是一个构造函数，接收一个函数作为参数，这个函数用于处理异步任务，且需要传递两个参数：

（1）resolve：异步操作执行成功后的回调函数

（2）reject：异步操作执行失败后的回调函数

##### then的用法

通过Promise.then获取处理结果，then方法可以接收两个参数，第一个对应resolve的回调，第一个对应reject的回调。Promise.then中的函数是异步执行的。

##### catch的用法

和then的第二个参数一样，用来指定reject的回调。

另一个作用：在执行resolve的回调时，如果抛出异常了，那么并不会报错卡死，而是会进到catch方法中执行reject的回调。

##### all的用法

Promise.all接收一个数组参数，里面的值最终都返回Promise对象。利用Promise.all可以并行执行多个异步操作，并且在一个回调中处理所有的返回数据。

##### race的用法

Promise.race()并发处理多个异步任务，只要有一个任务完成就能得到结果。



#### 箭头函数

##### 箭头函数与普通函数的区别

- 语法更简洁、清新
- 箭头函数不会创建自己的this（指向在定义时所处的外部执行环境的this）
- call()、apply()、bind()无法改变箭头函数中this的指向（箭头函数继承而来的this指向永远不变）
- 箭头函数不能作为构造函数使用
- 箭头函数没有自己的arguments
- 箭头函数没有原型prototype
- 箭头函数不能用作Generator函数，不能使用yield关键字



### Vue

#### 组件间的通信

props:用于父子组件通信
插槽:父子
自定义事件:子父@on，@emit，可以实现子给父通信
全局事件总线$bus:万能
pubsub:万能，vue当中几乎不用
Vuex:万能
$ref:父子通信

#### 路由



### Node.js常用模块

Node.js作为一个JavaScript的运行环境，提供了基础的功能和API，是一个渐进式框架：一个功能对应一个模块(js文件)，需要用的时候导入即可。

- 非渐进式框架：套餐，一次性导入所有的功能。无论是项目需要的还是不需要的(浪费资源)。
- 渐进式框架：自助餐，吃什么用什么，不浪费(节省资源)。

#### 内置模块

- fs文件系统模块
- path路径模块
- http模块

#### 自定义模块

用户创建的每个js文件都是自定义模块

#### 第三方模块

由第三方开发出来的模块，并非官方提供的内置模块，也不是用户创建的自定义模块，使用前需要下载。

#### Epress实现服务端功能

Express是专门用来创建服务器的。

```js
// 1. 导入express
const express = require('express')
// 2. 创建 web 服务器
const app = express()
// 3. 调用app.listen(端口号，启动成功后的回调函数)，启动服务器
app.listen(80, () => {
    console.log('express server running at http://127.0.0.1')
})
```



### Axios

#### 请求拦截

#### CORS

### Git、浏览器开发者工具



### 尚品汇

•  项目描述：此项目为在线电商Web App，包括首页、搜索列表、商品详情、用户登录/注册等多个模块
•  技术栈：Vue全家桶 + ES6 + Webpack + Axios
•  项目内容：

1. 使用 编程式导航路由 + 事件委派 + 自定义属性 实现搜索页面的跳转

   **answer**

   **编程式导航路由**

   路由的跳转有两种方式：声明式导航，编程式导航。

   使用声明式导航会出现卡顿现象。因为router-link是一个组件，相当于VueComponent类的实例对象。一瞬间new VueComponent很多实例，很消耗内存，因此导致卡顿。

   因此采用编程式导航进行路由跳转。（好处：可以书写自己的业务逻辑）。

   

   **事件委派**

   TyprNav三级联动菜单，点击a链接实现搜索页面跳转。

   

   **分析**

   点击三级菜单中的a链接都将跳转到搜索页面。利用**事件委派**，给三级菜单的父元素绑定路由跳转点击事件。

   **产生新的问题**

   事件委派满足了需求，但同时引发了新的问题：

   （1）事件委派是把全部子节点的事件委派给父节点(不仅是a标签，还有h3，dt，dl，em)。但是只有点击a标签的时候才会进行路由的跳转，**此时不能确定点击的一定是a标签**。

   （2）即使能确定点击的是a标签，如何区分点击的是一级，二级还是三级的a标签又是一个问题。

   **解决【自定义属性】**

   （1）给子节点当中的a标签，添加**自定义属性data-categoryName**，其余的子节点是没有的。判断标签身上是否有categoryname，如果存在则一定是a标签。

   （2）分别给一级、二级、三级a标签添加category1Id、category2Id、category3Id自定义属性可以区分出不能级的a标签。

   ```js
   // 进行路由跳转【home→search】的方法
         goSearch(event) {
             // 最好的解决方案：编程式导航路由+事件委派+自定义属性
             // 利用事件委派存在的问题：1. 事件委派，是把全部的子节点[h3,dt,dl,em]的事件委派给父节点
             // 点击a标签的时候，才会进行路由跳转【怎么能确定点击的一定是a标签】
             // 2. 即使能确定点击的是a标签，如何区分是一级、二级、三级分类的标签。
             // 解决第一个问题：把子节点当中a标签，加上自定义属性data-categoryName，其余的子节点是没有的
           let element = event.target
           // 获取到当前触发这个事件的节点【h3,a,dt,dl】，需要带有data-categoryName这样的节点【一定是a标签】
           // 节点有一个dataset属性，可以获取节点的自定义属性与属性值
           let {categoryname, category1id, category2id, category3id} = element.dataset
           // 如果标签身上拥有categoryname一定是a标签
           if(categoryname) {
               // 整理路由跳转的参数
               let location = {name: 'search'}
               let query = {categoryName: categoryname}
               // 一级分类、二级分类、三级分类的a标签
               if(category1id) {
                   query.category1Id = category1id
               }else if(category2id) {
                   query.category2Id = category2id
               } else {
                   query.category3Id = category3id
               }
               // 判断：如果路由跳转的时候，带有params参数，捎带传递过去
               if (this.$route.params) {
                   location.params = this.$route.params
                   // 整理完参数
                   location.query = query
                   // 路由跳转
                   this.$router.push(location)
               }
           }
         }
   ```

   

2. 使用lodash插件提供的防抖和节流功能来减少事件处理函数的调用频率，提升用户体验

   **answer**

   按需加载引入lodash

   ```js
   import throttle from 'lodash/throttle'
   ```

   TyprNav三级联动菜单，鼠标进入一级菜单事件。事件处理函数：当鼠标进入一级菜单，将鼠标当前索引等于鼠标移上某一个一级分类元素的索引值。

   **分析**

   正常情况（用户慢慢的操作）：鼠标进入每一个一级分类，都会触发鼠标进入事件；

   非正常情况（用户操作很快）：由于用户的行为过快，导致浏览器反应不过来，如果当前的回调函数中有一些大量的业务，有可能出现卡顿现象。（本身全部的一级分类都应该触发鼠标进入事件，但是经过测试，只有部分被触发了）

   **解决【节流】**

   节流：在规定的间隔时间内不会重复触发回调，只有大于这个时间间隔才会触发回调，把频繁触发变为少量触发

   防抖：前面的所有的触发都被取消，最后一次执行在规定的时间之后才会触发，也就是说如果连续快速的触发 只会执行最后一次

   **总结：【闭包+延时】**

   防抖：用户操作很频繁，但是只是执行一次

   节流：用户操作很频繁，但是把频繁的操作变为少量操作【可以给浏览器充裕的时间去解析代码】

   ```js
   changeIndex: throttle(function(index) {
       this.currentIndex = index
   }, 50)
   ```


​      

3. 使用Vuex模块式开发管理项目的数据，让数据分类更加明确；使用mock模块实现模拟数据

   **answer**

   （1）Vuex经常用的套路是state、mutations、actions、getters、modules

   （2）当后端开发人员没有写好接口时，前端开发人员可以mock一些数据，即模拟一些假的接口，在开发项目时可以把它当成真实的接口看待。在工作中项目上线时，需要把mock数据变为后台开发人员提供的接口数据。

   **第一步**:安装依赖包mockjs

   **第二步**：在src文件夹下创建一个文件夹，文件夹mock文件夹。

      **第三步**:准备模拟的数据(json数据，mock文件夹中创建相应的JSON文件)----格式化一下，别留有空格
      把mock数据需要的图片放置于public文件夹中！【public文件夹在打包的时候，会把相应的资源原封不动打包到dist文件夹中】
      比如:listContainer中的轮播图的数据
      [
         {id:1,imgUrl:'xxxxxxxxx'}, 
         {id:2,imgUrl:'xxxxxxxxx'}, 
         {id:3,imgUrl:'xxxxxxxxx'}, 
   ]

      **第四步**：在mock文件夹中创建一个server.js文件
      注意：在server.js文件当中对于banner.json||floor.json的数据没有暴露，但是可以在server模块中使用。
   对于webpack当中一些模块：图片、json数据格式，不需要对外暴露，因为**默认就是对外暴露**。

   **第五步**:通过mock模块模拟出数据

   通过Mock.mock方法进行模拟数据

      **第六步**:回到入口文件，引入serve.js（至少需要执行一次，才能模拟数据）
      mock需要的数据|相关mock代码页书写完毕，关于mock当中serve.js需要执行一次，
   如果不执行，和你没有书写一样的。

      **第七步**:在API文件夹中创建mockRequest【axios实例：baseURL:'/mock'】
   专门获取模拟数据用的axios实例。

4. 使用Swiper + watch + $nextTick实现轮播图效果

   **QA**

   问：swiper可以在移动端使用，还是在PC端使用？

   答：swiper移动端可以使用，pc端也可以使用。

   问：swiper常用于哪些场景？

   答：常用的场景为轮播图----【carousel：轮播图】

   

      **Swiper使用步骤：**
      第一步：引入依赖包【swiper.js|swiper.css】
      第二步:   静态页面中结构必须完整【container、wrap、slider】，类名不能瞎写
   第三步:   初始化swiper实例【轮播图添加动态效果】

   **问题**

   在**mounted**【组件实例挂载完毕】中初始化swiper实例，轮播图没有实现动态效果。（初始化swiper实例之前，页面中的结构务必要有）

   **原因**

   Swiper需要获取到轮播图的节点DOM，才能给swiper轮播添加动态效果，在mounted中，首先向vuex派发了action，ajax向服务器发请求涉及到异步语句，导致v-for遍历轮播图的时候结构还不完整，因此没有动态效果。

   **解决【mounted→watch】**

   watch监听属性可以监测到属性值的变化，当属性值发生变化的时候，可以触发一次。

   组件实例在使用仓库中的bannerList，组件的这个属性一定是bannerList一定是发生过变化，bannerList初始值是空数组，当服务器的数据返回以后，它的bannerList存储的属性值会发生变化【变为服务器返回的数据】，watch可以监听到。

   **还有一个问题**

   watch虽然可以监听到bannerList的变化，但是无法保证v-for已经执行结束了，只有当v-for执行完毕了才有结构。

   **解决【$nextTick】**

   组件实例的一个方法$nextTick

      nextTick官网解释:
      在下次DOM更新, 循环结束之后,执行延迟回调。在 修改数据之后 立即使用这个方法，获取更新后的DOM。
   注意：组件实例的$nextTick方法，在工作当中经常使用，经常结合第三方插件使用，获取更新后的DOM节点

   总结:$nextTick可以保留页面中的结构是一定有的，经常和很多插件一起使用【都需要DOM存在】。

      ```js
      watch: {
              // 监听bannerList数据的变化：因为这条数据发生过变化，由一个空数组变为数组里面有四个元素
              bannerList: {
                  immediate: true,
                  handler(newValue, oldValue) {
                      // 现在咱们通过watch监听bannerList属性的属性值的变化
                      // 如果执行handler方法，代表组件实例的身上这个属性应该有值了【四个元素的数组】
                      // 当前这个函数执行：只能保证bannerList的数据已经有了，但是没有办法保证v-for已经执行结束了【v-for执行也很耗时间】
                      // v-for执行完毕了才有结构【在watch当中没办法保证】
                      // nextTick：在下次DOM更新 循环结束之后 执行延迟回调。在 修改数据 之后，立即使用这个方法，获取更新后的DOM
                      this.$nextTick(() => { 
                          // 当你执行这个回调的时候，保证服务器数据回来了，v-for执行完毕了【轮播图的结构一定有了】初始化swiper实例对象
                          var mySwiper = new Swiper(this.$refs.mySwiper, {
                              loop: true,
                              // 如果需要分页器
                              pagination: {
                                  el: ".swiper-pagination",
                                  // 点击小球的时候也切换图片
                                  clickable: true
                              },
                              // 如果需要前进后退按钮
                              navigation: {
                                  nextEl: ".swiper-button-next",
                                  prevEl: ".swiper-button-prev",
                              }
                          });
                      });
                  }
              }
          }
      ```

   

5. 封装分页器全局组件

   对于分页器而言，自定义前提需要知道四个前提条件：

   （1）pageNo：当前在第几页

   （2）pageSize：代表每一页展示多少条数据

   （3）total：代表整个分页器一共要展示多少条数据

   （4）continue：代表分页连续页码个数

   分页器动态展示，分为上中下三个部分

      ```vue
      <template>
        <div class="pagination">
          <!-- 测试用的数据 -->
          <!-- <h1>{{startNumAndEndNum}}-----当前的页码{{pageNo}}</h1> -->
          <!-- 上 -->
          <button :disabled="pageNo==1" @click="$emit('getPageNo',pageNo-1)">上一页</button>
          <button 
          v-if="startNumAndEndNum.start > 1" 
          @click="$emit('getPageNo',1)" 
          :class="{active: pageNo==1}"
          >
            1
          </button>
          <button v-if="startNumAndEndNum.start > 2">···</button>
      
          <!-- 中间部分 -->
          <button v-for="(page,index) in startNumAndEndNum.end" 
          :key="index" 
          v-if="page>=startNumAndEndNum.start" 
          @click="$emit('getPageNo',page)" 
          :class="{active: pageNo==page}"
          >
            {{page}}
          </button>
          <!-- <button>3</button>
          <button>4</button>
          <button>5</button>
          <button>6</button>
          <button>7</button> -->
          
          <!-- 下 -->
          <button v-if="startNumAndEndNum.end < totalPage - 1">···</button>
          <button 
          v-if="startNumAndEndNum.end < totalPage" 
          @click="$emit('getPageNo',totalPage)" 
          :class="{active: pageNo==totalPage}"
          >
            {{totalPage}}
          </button>
          <button :disabled="pageNo==totalPage" @click="$emit('getPageNo',pageNo+1)">下一页</button>
          
          <button style="margin-left: 30px">共 {{total}} 条</button>
        </div>
      </template>
      
      <script>
        export default {
          name: "Pagination",
          props: ['pageNo', 'pageSize', 'total', 'continues'],
          computed: {
            // 总共多少页
            totalPage() {
              // 向上取整
              return Math.ceil(this.total / this.pageSize)
            },
            // 计算出连续的页码的起始数字与结束数字[连续页码的数字：至少是5]
            startNumAndEndNum() {
              const {continues, pageNo, totalPage} = this
              // 先定义两个变量存储起始数字与结束数字
              let start = 0, end = 0
              // 连续的页码时5,【就是至少五页】如果出现不正常的现象【就是不够五页】
              // 不正常现象【总页码数没有连续页码多】
              if(continues > totalPage) {
                start = 1
                end = totalPage
              } else {
                // 正常现象【连续页码5，但是总页数一定是大于5的】
                // 起始数字
                start = pageNo - parseInt(continues / 2)
                // 结束数字
                end = pageNo + parseInt(continues / 2)
                // 把出现不正常的现象【start数字出现0|负数】纠正
                if(start < 1) {
                  start = 1,
                  end = continues
                }
                // 把出现不正常的现象【end数字大于总页码的】
                if (end > totalPage) {
                  end = totalPage,
                  start = totalPage - continues + 1
                }
              }
              return {start, end}
            }
          }
        }
      </script>
      ```

   

6. 利用路由传参结合会话存储跳转到购物车加入成功页面

   **在路由跳转的时候需要将产品信息以及id带给下一级路由**

   可以用下面这种手段实现路由跳转以及传递参数：

   ```js
   this.$router.push({name: 'addcartsuccess',query: {skuInfo: this.skuInfo,skuNum: this.skuNum}})
   ```

   **其中产品信息skuInfo是一个对象，在地址栏中会转成字符串看着不美观，可以利用会话存储将产品信息存储到浏览器中**

   ```js
   // 本地存储|会话存储一般存储的是字符串，因为需要将其转换成字符串形式
   sessionStorage.setItem("SKUINFO",JSON.stringify(this.skuInfo))
   // 一些简单的数据skuNum，通过query形式给路由组件传递过去，产品信息数据比较复杂，通过会话存储
   this.$router.push({name: 'addcartsuccess',query:{skuNum: this.skuNum}})
   ```

   **会话存储的特点：存储不持久化，会话结束后数据再消失。对于该项目需求，会话存储即可达到目的，使用本地存储是没有必要的。**

   

7. 使用uuidv4封装游客身份模块，通过请求头将临时身份带给服务器，存储用户购物车数据

   **问题**

   向服务器发请求获取购物车数据，请求成功，但是购物车数据为空

   **原因**

   只是向服务器存储了用户数据，但是服务器并不知道存储的这些数据属于谁。

   **解决**

   **解决思路：**在用户将商品添加到购物车时(商品详情页)，需要将用户的临时身份信息携带给服务器，告知服务器产品ID和数量属于哪个用户，把数据存储于相应的用户中。

   **具体办法：**uuidv4生成一个随机字符串，每次都会发生变化，但是游客的身份不能改变，因此需要结合本地存储localStorage封装游客身份模块，作为用户唯一的标识。但是请求获取购物车接口只带有两个参数产品id和产品个数，没有uuid参数，不能通过接口携带。因此需要通过请求头将临时身份携带给服务器(添加userTemp字段)，从而存储用户购物车数据。

   

   **新的问题**

   游客身份在仓库中，ajax请求模块中拿不到游客身份

   **解决**

   要在请求拦截器中捞到仓库

   ```js
   // 在axios二次封装模块中引入仓库
   import store from "@/store"
   
   requests.interceptors.request.use(config => {
     // config: 配置对象，对象里面有一个属性很重要，headers请求头
     if (store.state.detail.uuid_token) {
       // 给请求头添加一个字段(userTempId)：和后台商量好了，不能随便写
       config.headers.userTempId = store.state.detail.uuid_token
     }
     // 需要携带token带给服务器
     if (store.state.user.token) {
       config.headers.token = store.state.user.token
     }
     // 进度条开始滚动
     nprogress.start()
     return config
   })
   ```

   

8. 通过给请求头添加token字段，将token的值携带给服务器，获取用户唯一标识，从而返回用户登录信息。

   **问题**

   向服务器发请求获取用户登录信息，请求成功，但是请求返回未登录

   **原因**

   虽然发起了“获取用户登录信息”请求(平台首页)，但是服务器需要知道是谁需要用户信息才能返回相应的登录信息。因为请求没有携带token参数给服务器，所以服务器认为用户没有登录，因此获取不到用户的信息。

   **解决**

   在请求拦截器中给请求头添加token字段，发请求的时候把token携带给服务器。

9. 不使用vuex仓库，直接在组件中发请求获取数据，数据初始值存储到data中

10. Element-UI按需引入实现支付页面部分业务(遮罩层)

    



--------------------------------------------------------------

### 项目性能优化

（1）TypeNav三级联动性能优化

**问题**

home切换到search或者search切换到home，组件在频繁的向服务器发请求，获取三级联动的数据进行展示。项目中如果频繁的向服务器发请求，很耗性能的，因此需要进行优化。

为什么会频繁的向服务器发请求获取三级联动的数据呢？

因为路由跳转的时候，组件会进行销毁的【home组件的created：在向vuex派发action，因此频繁的获取三级联动的数据】

**解决**

只需要发一次请求，获取到三级联动的数据即可，不需要多次。

答：在App根组件当中发请求【根组件mounted】执行一次

（main.js也是执行一次，但是不可以放在它里面，因为它不是一个组件(以.vue结尾)，而是一个js文件，this是undefined）

（2）v-if | v-show选择

（3）按需加载

（4）防抖与节流：请求次数优化

（5）search搜索页面请求的性能优化

发一个请求，需要向服务器携带参数：带100个参数 带1个参数【消耗宽带】。对于给服务器携带的参数，如果数值为undefined，向服务器发请求时，参数不会携带给服务器的。



### 科研成果

