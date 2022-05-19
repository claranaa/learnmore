### 初识Vue

```html
<body>
	<!-- 准备好一个容器 -->
	<div id="demo">
		<h1>Hello，{{name.toUpperCase()}}，{{address}}</h1>
	</div>

	<script type="text/javascript" >
    	//阻止 vue 在启动时生成生产提示。
		Vue.config.productionTip = false 
		//创建Vue实例
		new Vue({
			el:'#demo', //el用于指定当前Vue实例为哪个容器服务，值通常为css选择器字符串。
			data:{ //data中用于存储数据，数据供el所指定的容器去使用，值我们暂时先写成一个对象。
				name:'atguigu',
				address:'北京'
				}
			})
	</script>
```

#### 初识Vue：

（1）想要让Vue工作，就必须创建一个Vue实例，且要传入一个配置对象；

（2）root容器里的代码依然符合html规范，只不过混入了一些特殊的Vue语法；

（3）root容器里的代码被称为【Vue模板】

（4）Vue实例和容器是一一对应的；

（5）真实开发中只有一个Vue实例，并且会配合着组件一起使用；

（6）{{xxx}}中xxx要写js表达式，且xxx可以自动读取到data中的所有属性；

（7）一旦data中的数据发生改变，那么页面中用到该数据的地方也会自动更新。

#### 注意区分：js表达式和js代码(语句)

- 表达式：一个表达式会产生一个值，可以放在任何一个需要值的地方：

  （1）a

  （2）a+b

  （3）demo(1)

  （4）x === y ? ‘a’ : ‘b’

- js代码(语句)

  （1）if() {}

  （2）for() {}

### 模板语法

```html
<body>
    <div id="root">
		<h1>插值语法</h1>
		<h3>你好，{{name}}</h3>
		<hr/>
		<h1>指令语法</h1>
		<a v-bind:href="school.url.toUpperCase()" x="hello">点我去{{school.name}}学习1</a>
		<a :href="school.url" x="hello">点我去{{school.name}}学习2</a>
	</div>
</body>

	<script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		new Vue({
			el:'#root',
			data:{
				name:'jack',
				school:{
					name:'尚硅谷',
					url:'http://www.atguigu.com',
				}
			}
		})
	</script>
</body>
```

#### Vue模板语法有两大类

- 插值语法：

  功能：用于解析标签体内容

  写法：{{xxx}}，xxx是js表达式，且可以直接读取到data中的所有属性

- 指令语法：

  功能：用于解析标签（包括：标签属性、标签体内容、绑定事件.....）。

  举例：v-bind:href="xxx" 或  简写为 :href="xxx"，xxx同样要写js表达式，且可以直接读取到data中的所有属性。

  备注：Vue中有很多的指令，且形式都是：v-????，此处v-bind是一个例子。

### 数据绑定

```html
<body>
    <div id="root">
		<!-- 普通写法 -->
		<!-- 单向数据绑定：<input type="text" v-bind:value="name"><br/>
		双向数据绑定：<input type="text" v-model:value="name"><br/> -->

		<!-- 简写 -->
		单向数据绑定：<input type="text" :value="name"><br/>
		双向数据绑定：<input type="text" v-model="name"><br/>
		<!-- 如下代码是错误的，因为v-model只能应用在表单类元素（输入类元素）上 -->
		<!-- <h2 v-model:x="name">你好啊</h2> -->
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		new Vue({
			el:'#root',
			data:{
				name:'尚硅谷'
			}
		})
	</script>
</body>
```

#### 数据绑定的两种方式

- 单向绑定(v-bind)：数据只能从data流向页面

- 双向绑定(v-model)：数据不仅能从data流向页面，还可以从页面流向data

  注意：（1）双向绑定一般都应用在表单类元素上(如：input

  、select等)

  ​			（2）v-model：value可以简写为v-model，因为v-model默认收集的就是value的值

### el与data的两种写法

```html
<body>
    <div id="root">
		<h1>你好，{{name}}</h1>
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。

	//el的两种写法
	/* const v = new Vue({
		//el:'#root', //第一种写法
		data:{
			name:'尚硅谷'
		}
	})
	console.log(v)
	v.$mount('#root') //第二种写法mount挂载 */

	/* setTimeout(() => {
		v.$mount('root')
	}, 1000) */



	//data的两种写法
	new Vue({
		el: '#root',
		//data的第一种写法：对象式
		/* data:{
			name:'尚硅谷'
		} */

		//data的第二种写法：函数式
		data() {
			console.log('@@@', this) //此处的this是Vue实例对象
			return {
				name: '尚硅谷'
			}
		}
	})
</script>
</body>
```

- el的两种写法

  （1）new Vue时候配置el属性

  （2）先创建Vue实例，随后再通过vm.$mount(‘#root’)指定el的值

- data的两种写法

  （1）对象式

  （2）函数式

  如何选择：在用到组件时，data必须使用函数式，否则会报错

  一个重要原则：一定不要写箭头函数，一旦写了箭头函数，this就不再是Vue实例了，就是window了。

### MVVM模型

```html
<body>
    <div id="root">
		<h1>学校名称：{{name}}</h1>
		<h1>学校地址：{{address}}</h1>
		<!-- <h1>测试一下1：{{1+1}}</h1>
		<h1>测试一下2：{{$options}}</h1>
		<h1>测试一下3：{{$emit}}</h1>
		<h1>测试一下4：{{_c}}</h1> -->
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		const vm = new Vue({
			el:'#root',
			data:{
				name:'尚硅谷',
				address:'北京',
			}
		})
		console.log(vm)
	</script>
</body>
```

MVVM模型：

（1）M：模型(Model)：data中的数据

（2）V：视图(View)：模板代码

（3）VM：视图模型(ViewModel)：Vue实例

观察发现：

（1）data中所有的属性，最后都出现在了vm身上

（2）vm身上所有的属性及Vue原型上的所有属性，在Vue模板中都可以直接使用

### 数据代理

数据代理：通过一个对象代理对另一个对象中属性的操作(读/写)

```html
<body>
    <div id="root">
		<h2>学校名称：{{name}}</h2>
		<h2>学校地址：{{address}}</h2>
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		const vm = new Vue({
			el:'#root',
			data:{
				name:'尚硅谷',
				address:'宏福科技园'
			}
		})
	</script>
</body>
```

#### Vue中的数据代理

通过vm对象代理data对象中属性的操作(读/写)

#### Vue中数据代理的好处

更加方便的操作data中的数据

#### 基本原理

通过Object.defineProperty()把data对象中所有属性添加到vm上。

为每一个添加到vm上的属性，都指定一个getter/setter。

在getter/setter内部去操作（读/写）data中对应的属性。

### 事件处理

##### 事件的基本使用

```html
<body>
    <div id="root">
		<h2>欢迎来到{{name}}学习</h2>
		<!-- <button v-on:click="showInfo">点我提示信息</button> -->
		<button @click="showInfo1">点我提示信息1（不传参）</button>
		<button @click="showInfo2($event,66)">点我提示信息2（传参）</button>
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		const vm = new Vue({
			el:'#root',
			data:{
				name:'尚硅谷',
			},
			methods:{
				showInfo1(event){
					// console.log(event.target.innerText)
					// console.log(this) //此处的this是vm
					alert('同学你好！')
				},
				showInfo2(event,number){
					console.log(event,number)
					// console.log(event.target.innerText)
					// console.log(this) //此处的this是vm
					alert('同学你好！！')
				}
			}
		})
	</script>
</body>
```

1.使用v-on:xxx 或 @xxx 绑定事件，其中xxx是事件名；

2.事件的回调需要配置在methods对象中，最终会在vm上；

3.methods中配置的函数，不要用箭头函数！否则this就不是vm了；

4.methods中配置的函数，都是被Vue所管理的函数，this的指向是vm 或 组件实例对象；

 5.@click="demo" 和 @click="demo($event)" 效果一致，但后者可以传参；

##### 事件修饰符

1.prevent：阻止默认事件（常用）；

2.stop：阻止事件冒泡（常用）；

3.once：事件只触发一次（常用）；

4.capture：使用事件的捕获模式；

5.self：只有event.target是当前操作的元素时才触发事件；

6.passive：事件的默认行为立即执行，无需等待事件回调执行完毕；

##### 键盘事件

```html
<body>
    <div id="root">
		<h2>欢迎来到{{name}}学习</h2>
		<input type="text" placeholder="按下回车提示输入" @keydown.huiche="showInfo">
	</div>
    <script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		Vue.config.keyCodes.huiche = 13 //定义了一个别名按键
		new Vue({
			el:'#root',
			data:{
				name:'尚硅谷'
			},
			methods: {
				showInfo(e){
					// console.log(e.key,e.keyCode)
					console.log(e.target.value)
				}
			},
		})
	</script>
</body>
```

1.Vue中常用的按键别名：

​       回车 => enter

​       删除 => delete (捕获“删除”和“退格”键)

​       退出 => esc

​       空格 => space

​       换行 => tab (特殊，必须配合keydown去使用)

​       上 => up

​       下 => down

​       左 => left

​       右 => right

2.Vue未提供别名的按键，可以使用按键原始的key值去绑定，但注意要转为kebab-case（短横线命名）

3.系统修饰键（用法特殊）：ctrl、alt、shift、meta

​       (1).配合keyup使用：按下修饰键的同时，再按下其他键，随后释放其他键，事件才被触发。

​       (2).配合keydown使用：正常触发事件。

4.也可以使用keyCode去指定具体的按键（不推荐）

5.Vue.config.keyCodes.自定义键名 = 键码，可以去定制按键别名

### 计算属性

- 定义：要用的属性不存在，要通过已有属性计算得来。

- 原理：底层借助了Object.defineproperty方法提供的getter和setter。

- get函数什么时候执行？

  （1）初次读取时会执行一次。以后再调用就不读取了，因为有缓存。

  （2）当依赖的数据发生改变时会被再次调用。

- 优势：与methods实现相比，内部有缓存机制(可复用)，效率更高，调试方便。

- 注意：（1）计算属性最终会出现在vm上，直接读取使用即可。

  ​            （2）如果计算属性要被修改，那必须写set函数去响应修改，且set中要引起计算时依赖的数据发生改变。

```html
<body>
    <div id="root">
		姓：<input type="text" v-model="firstName"> <br /><br />
		名：<input type="text" v-model="lastName"> <br /><br />
		全名：<span>{{fullName}}</span> <br /><br />
	</div>
</body>
<script type="text/javascript">
	Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
	const vm = new Vue({
		el: '#root',
		data: {
			firstName: '张',
			lastName: '三'
		},
		computed: {
			fullName: {
				//get有什么作用？当有人读取fullName时，get就会被调用，且返回值就作为fullName的值
				//get什么时候调用？1.初次读取fullName时。2.所依赖的数据发生变化时。
				get() {
					console.log('get被调用了')
					// console.log(this) //此处的this是vm
					return this.firstName + '-' + this.lastName
				},
				//set什么时候调用? 当fullName被修改时。
				set(value) {
					console.log('set', value)
					const arr = value.split('-')
					this.firstName = arr[0]
					this.lastName = arr[1]
				}
			}
		}
	})
</script>
```

#### 计算属性的简写

```html
<script type="text/javascript">
	Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
	const vm = new Vue({
		el:'#root',
		data:{
			firstName:'张',
			lastName:'三',
		},
		computed:{
			//完整写法
			/* fullName:{
			get(){
				 console.log('get被调用了')
				return this.firstName + '-' + this.lastName
					},
					set(value){
						console.log('set',value)
						const arr = value.split('-')
						this.firstName = arr[0]
						this.lastName = arr[1]
					}
				} */
			//简写
			fullName(){
					console.log('get被调用了')
					return this.firstName + '-' + this.lastName
				}
			}
		})
</script>
```

### 监视属性/侦听属性

- 监视属性watch：

（1）当被监视的属性变化时，回调函数自动调用，进行相关操作

（2）监视的属性必须存在，才能进行监视！

- 监视的两种写法：

  （1）new Vue时传入watch配置

  （2）通过vm.$watch监视

```html
<body>
    <div id="root">
		<h2>今天天气很{{info}}</h2>
		<button @click="changeWeather">切换天气</button>
	</div>
</body>
<script type="text/javascript">
	Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
	const vm = new Vue({
		el:'#root',
		data:{
				isHot:true,
			},
		computed:{
				info(){
					return this.isHot ? '炎热' : '凉爽'
				}
			},
		methods: {
				changeWeather(){
					this.isHot = !this.isHot
				}
			},
		/* watch:{
				isHot:{
					immediate:true, //初始化时让handler调用一下
					//handler什么时候调用？当isHot发生改变时。
					handler(newValue,oldValue){
						console.log('isHot被修改了',newValue,oldValue)
					}
				}
			} */
		})
    // 第二种写法
		vm.$watch('isHot',{
			immediate:true, //初始化时让handler调用一下
			//handler什么时候调用？当isHot发生改变时。
			handler(newValue,oldValue){
				console.log('isHot被修改了',newValue,oldValue)
			}
		})
</script>
```

#### 深度监视

（1）Vue中watch默认不监测对象内部值的改变(一层)

（2）配置deep：true可以监测对象内部值改变(多层)

注意：

（1）Vue自身可以监测对象内部值的改变，但Vue提供的watch默认不可以！

（2）使用watch时根据数据的具体结构，决定是否采用深度监视。

```html
<body>
    <div id="root">
		<h2>今天天气很{{info}}</h2>
		<button @click="changeWeather">切换天气</button>
		<hr/>
		<h3>a的值是:{{numbers.a}}</h3>
		<button @click="numbers.a++">点我让a+1</button>
		<h3>b的值是:{{numbers.b}}</h3>
		<button @click="numbers.b++">点我让b+1</button>
		<button @click="numbers = {a:666,b:888}">彻底替换掉numbers</button>
		{{numbers.c.d.e}}
	</div>
</body>
<script type="text/javascript">
		Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
		const vm = new Vue({
			el:'#root',
			data:{
				isHot:true,
				numbers:{
					a:1,
					b:1,
					c:{
						d:{
							e:100
						}
					}
				}
			},
			computed:{
				info(){
					return this.isHot ? '炎热' : '凉爽'
				}
			},
			methods: {
				changeWeather(){
					this.isHot = !this.isHot
				}
			},
			watch:{
				isHot:{
					// immediate:true, //初始化时让handler调用一下
					//handler什么时候调用？当isHot发生改变时。
					handler(newValue,oldValue){
						console.log('isHot被修改了',newValue,oldValue)
					}
				},
				//监视多级结构中某个属性的变化
				/* 'numbers.a':{
					handler(){
						console.log('a被改变了')
					}
				} */
				//监视多级结构中所有属性的变化
				numbers:{
					deep:true,
					handler(){
						console.log('numbers改变了')
					}
				}
			}
		})

</script>
```

#### 监视属性简写

```html
<script type="text/javascript">
	Vue.config.productionTip = false //阻止 vue 在启动时生成生产提示。
	const vm = new Vue({
		el: '#root',
		data: {
			isHot: true,
		},
		computed: {
			info() {
				return this.isHot ? '炎热' : '凉爽'
			}
		},
		methods: {
			changeWeather() {
				this.isHot = !this.isHot
			}
		},
		watch: {
			//正常写法
			/* isHot:{
				// immediate:true, //初始化时让handler调用一下
				// deep:true,//深度监视
				handler(newValue,oldValue){
					console.log('isHot被修改了',newValue,oldValue)
				}
			}, */
			//简写
			/* isHot(newValue,oldValue){
				console.log('isHot被修改了',newValue,oldValue,this)
			} */
		}
	})

		//正常写法
	/* vm.$watch('isHot',{
		immediate:true, //初始化时让handler调用一下
		deep:true,//深度监视
		handler(newValue,oldValue){
			console.log('isHot被修改了',newValue,oldValue)
		}
	}) */

		//简写
	/* vm.$watch('isHot',function(newValue,oldValue) {
		console.log('isHot被修改了',newValue,oldValue,this)
	}) */
</script>
```

#### computed和watch之间的区别

- computed能完成的功能，watch都可以完成

- watch能完成的功能，computed不一定能完成，例如：watch可以进行异步操作。

- 两个重要的原则：

  （1）被Vue管理的函数，最好写成普通函数，这样this的指向才是vm或组件实例对象。

  （2）不被Vue管理的函数(定时器的回调函数、ajax的回调函数等、Promise的回调函数)，最好写成箭头函数，这样this的指向才是vm或组件实例对象。

### 绑定样式

- class样式

  写法：:class=“xxx” xxx可以是字符串、对象、数组。

  数组写法适用于：要绑定多个样式，个数不确定，名字也不确定。

  对象写法适用于：要绑定多个样式，个数确定，名字也确定，但不确定用不用。

- style样式

  :style=“{fontSize: xxx}”其中xxx是动态值。

  :style=“[a, b]”其中a、b是样式对象。

```html
<body>
    <div id="root">
		<!-- 绑定class样式--字符串写法，适用于：样式的类名不确定，需要动态指定 -->
		<div class="basic" :class="mood" @click="changeMood">{{name}}</div> <br /><br />

		<!-- 绑定class样式--数组写法，适用于：要绑定的样式个数不确定、名字也不确定 -->
		<div class="basic" :class="classArr">{{name}}</div> <br /><br />

		<!-- 绑定class样式--对象写法，适用于：要绑定的样式个数确定、名字也确定，但要动态决定用不用 -->
		<div class="basic" :class="classObj">{{name}}</div> <br /><br />

		<!-- 绑定style样式--对象写法 -->
		<div class="basic" :style="styleObj">{{name}}</div> <br /><br />
		<!-- 绑定style样式--数组写法 -->
		<div class="basic" :style="styleArr">{{name}}</div>
	</div>
</body>
<script type="text/javascript">
	Vue.config.productionTip = false

	const vm = new Vue({
		el: '#root',
		data: {
			name: '尚硅谷',
			mood: 'normal',
			classArr: ['atguigu1', 'atguigu2', 'atguigu3'],
			classObj: {
				atguigu1: false,
				atguigu2: false,
			},
			styleObj: {
				fontSize: '40px',
				color: 'red',
			},
			styleObj2: {
				backgroundColor: 'orange'
			},
			styleArr: [
				{
					fontSize: '40px',
					color: 'blue',
				},
				{
					backgroundColor: 'gray'
				}
			]
		},
		methods: {
			changeMood() {
				const arr = ['happy', 'sad', 'normal']
				const index = Math.floor(Math.random() * 3)
				this.mood = arr[index]
			}
		},
	})
</script>
```

### 条件渲染

1.v-if

​          写法：

​            (1).v-if="表达式"

​            (2).v-else-if="表达式"

​            (3).v-else="表达式"

​          适用于：切换频率较低的场景。

​          特点：不展示的DOM元素直接被移除。

​          注意：v-if可以和:v-else-if、v-else一起使用，但要求结构不能被“打断”。

​       2.v-show

​          写法：v-show="表达式"

​          适用于：切换频率较高的场景。

​          特点：不展示的DOM元素未被移除，仅仅是使用样式隐藏掉display：none

​       3.注意：

​		（1）使用v-if的时，元素可能无法获取到，而使用v-show一定可以获取到。

​		（2）只有v-if可以和template搭配使用

```html
<div id="root">
		<h2>当前的n值是:{{n}}</h2>
		<button @click="n++">点我n+1</button>
		<!-- 使用v-show做条件渲染 -->
		<!-- <h2 v-show="false">欢迎来到{{name}}</h2> -->
		<!-- <h2 v-show="1 === 1">欢迎来到{{name}}</h2> -->

		<!-- 使用v-if做条件渲染 -->
		<!-- <h2 v-if="false">欢迎来到{{name}}</h2> -->
		<!-- <h2 v-if="1 === 1">欢迎来到{{name}}</h2> -->

		<!-- v-else和v-else-if -->
		<!-- <div v-if="n === 1">Angular</div>
		<div v-else-if="n === 2">React</div>
		<div v-else-if="n === 3">Vue</div>
		<div v-else>哈哈</div> -->

		<!-- v-if与template的配合使用 -->
			<template v-if="n === 1">
				<h2>你好</h2>
				<h2>尚硅谷</h2>
				<h2>北京</h2>
			</template>
</div>
```

