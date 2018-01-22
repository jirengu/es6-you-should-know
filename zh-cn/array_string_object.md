# 数组、字符串、对象

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




