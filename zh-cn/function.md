## 函数
1. 默认值

```javascript
function sayHi(name='jirengu') {
  console.log(`hi, ${name}`)
}
sayHi()
sayHi('ruoyu')
```

```javascript
function fetch(url, { body='', method = 'GET', headers = {} } = {}) {
  console.log(method);
}

fetch('http://example.com')
```

以下两种写法的区别?

```javascript
//ex1
function m1({x = 0, y = 0} = {}) {
  return [x, y];
}

//ex2 
function m2({x, y} = { x: 0, y: 0 }) {
  return [x, y];
}

// 函数没有参数的情况
m1() // [0, 0]
m2() // [0, 0]

// x 和 y 都有值的情况
m1({x: 3, y: 8}) // [3, 8]
m2({x: 3, y: 8}) // [3, 8]

// x 有值，y 无值的情况
m1({x: 3}) // [3, 0]
m2({x: 3}) // [3, undefined]

// x 和 y 都无值的情况
m1({}) // [0, 0];
m2({}) // [undefined, undefined]

m1({z: 3}) // [0, 0]
m2({z: 3}) // [undefined, undefined]
```

ex1： 调用函数需要你传递一个对象，如果你没传对象就用默认值对象`{}`，默认值对象里面都是 undefined， 所以属性使用初始值

ex2：参数需要是一个对象，如果没传对象，就用默认值对象`{ x: 0, y: 0 }`如果传了对象，就使用你传递的对象

3. 箭头函数

```javascript
var f = v => v+1
//等价于
var f = function(v){return v+1}

var f = () => 5;
// 等同于
var f = function () { return 5 };

var sum = (num1, num2) => num1 + num2;
// 等同于
var sum = function(num1, num2) {
  return num1 + num2;
};

var arr = [1, 2, 3]
var arr2 = arr.map(v=>v*v)
arr2 //[1, 4, 9]

```

箭头函数里面的 this 

```javascript
// ES6
function foo() {
  setTimeout(() => {
    console.log('id:', this.id);
  }, 100);
}

//  等同于如下ES5
function foo() {
  var _this = this;
  setTimeout(function () {
    console.log('id:', _this.id);
  }, 100);
}
```

## 对象

```javascript
var name = 'jirengu'
var age = 3
var people = {name, age} //{name:'jirengu', age:3}
```

```javascript
let app = {
   selector: '#app',
   init() {
   },
   bind() {
   } 
}
app.init()

``



## 字符串
1. 多行字符串

```javascript
let str =`
Hi,
This is jirengu.com.
You can study frontend here.
`
```

2. 字符串模板

```javascript
let website = 'jirengucom'
let who = 'You'
let str = `Hi
This is ${website}.
${who} can study frontend here
`
```
## 数组
1. 扩展

```javascript
var a = [1, 2]
console.log(...a)  // 1, 2
var b = [...a, 3]
b // [1, 2, 3]

var c = b.concat([4, 5])
var d = [...b, 4, 5]
```

2. 函数参数的扩展

```javascript
function sort(...arr){
  console.log(arr.sort())
}
sort(3, 1, 5)  //[1, 3, 5]
```

```javascript
function max(arr){
  return Math.max(...arr)
}
max([3, 4, 1])  // 4
```

3. 类数组对象转数组

```javascript
let ps = document.querySelectorAll('p');
Array.from(ps).forEach(p=> {
  console.log(p.innerText);
});
[...ps].forEach(p=>{console.log(p.innerText)});
```

## 函数
1. 默认值

```javascript
function sayHi(name='jirengu') {
  console.log(`hi, ${name}`)
}
sayHi()
sayHi('ruoyu')
```

```javascript
function fetch(url, { body='', method = 'GET', headers = {} } = {}) {
  console.log(method);
}

fetch('http://example.com')
```

以下两种写法的区别?

```javascript
//ex1
function m1({x = 0, y = 0} = {}) {
  return [x, y];
}

//ex2 
function m2({x, y} = { x: 0, y: 0 }) {
  return [x, y];
}

// 函数没有参数的情况
m1() // [0, 0]
m2() // [0, 0]

// x 和 y 都有值的情况
m1({x: 3, y: 8}) // [3, 8]
m2({x: 3, y: 8}) // [3, 8]

// x 有值，y 无值的情况
m1({x: 3}) // [3, 0]
m2({x: 3}) // [3, undefined]

// x 和 y 都无值的情况
m1({}) // [0, 0];
m2({}) // [undefined, undefined]

m1({z: 3}) // [0, 0]
m2({z: 3}) // [undefined, undefined]
```

ex1： 调用函数需要你传递一个对象，如果你没传对象就用默认值对象`{}`，默认值对象里面都是 undefined， 所以属性使用初始值

ex2：参数需要是一个对象，如果没传对象，就用默认值对象`{ x: 0, y: 0 }`如果传了对象，就使用你传递的对象

3. 箭头函数

```javascript
var f = v => v+1
//等价于
var f = function(v){return v+1}

var f = () => 5;
// 等同于
var f = function () { return 5 };

var sum = (num1, num2) => num1 + num2;
// 等同于
var sum = function(num1, num2) {
  return num1 + num2;
};

var arr = [1, 2, 3]
var arr2 = arr.map(v=>v*v)
arr2 //[1, 4, 9]

```

箭头函数里面的 this 

```javascript
// ES6
function foo() {
  setTimeout(() => {
    console.log('id:', this.id);
  }, 100);
}

//  等同于如下ES5
function foo() {
  var _this = this;
  setTimeout(function () {
    console.log('id:', _this.id);
  }, 100);
}
```

## 对象

```javascript
var name = 'jirengu'
var age = 3
var people = {name, age} //{name:'jirengu', age:3}
```

```javascript
let app = {
   selector: '#app',
   init() {
   },
   bind() {
   } 
}
app.init()

``
