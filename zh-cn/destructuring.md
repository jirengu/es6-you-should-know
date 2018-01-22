# 解构赋值
## 1. 数组的解构

```javascript
let [a,b,c] = [1,2,3]
console.log(a, b, c) 

let [a, [b], c] = [2, [3], 4]
a //2
b //3
c //4

let [a] = 1 //报错
```
## 2. 默认值

```javascript
let [a, b = 2] = [3]
a // 3
b // 2

let [a, b = 2] = [3, 4]
a //3
b //4
```

数组对应对值有没有？如果没有（数组对没有指undefined）就使用默认值，如果有就使用对应值

```javascript
let [a=2, b=3] = [undefined, null]
a //2
b //null
```

```javascript
let [a=1, b=a] = [2]
a //2
b //2
```
## 3. 对象的解构赋值
前置知识

```javascript
let [name, age] = ['hunger', 3]
let p1 = {name, age}
//等同于
let p2 = {name: name, age: age}
```

解构范例

```javascript
let {name, age} = {name: 'jirengu', age: 4}
name //‘jirengu’
age //4
```

以上代码等同于

```javascript
let name
let age
({name: name, age: age} = {name: 'jirengu', age: 4})
```
## 4. 默认值

```javascript
let {x, y=5} = {x: 1}
x //1
y //5
```
## 5. 函数解构

```javascript
function add([x=1, y=2]){
  return x+y
}
add() //Error
add([2]) //4
add([3,4]) //7

function sum({x, y}={x:0, y:0}, {a=1, b=1}){
    return [x+a, y+b]
}
sum({x:1, y:2}, {a:2}) //[3, 3]
```
## 6. 作用

```javascript
let [x, y] = [1, 2];
[x, y] = [y, x]
x //2
y // 1
```

```javascript
function ajax({url, type=‘GET’}){
}
ajax({url: ‘http://localhost:3000/getData’})
```











