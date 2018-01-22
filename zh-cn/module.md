# 模块化
## 写法1

```javascript
// profile.js
export var firstName = 'Michael';
export var lastName = 'Jackson';
export var year = 1958;
```

```javascript
//useage.js
import {firstName, lastName, year} from './profile';
console.log(firstName)
```
## 写法2

```javascript
var firstName = 'Michael';
var lastName = 'Jackson';
var year = 1958;

export {firstName, lastName, year};
```

```javascript
//useage.js
import {firstName, lastName, year} from './profile';
console.log(firstName)
```

## 写法3

```javascript
//helper.js
export function getName(){}
export function getYear(){}
```

```javascript
//main.js
import {getName, getYear} from './helper';
getName()
```


## 写法4

```javascript
//helper.js
function getName(){}
function getYear(){}
export {getName, getYear}
```

```javascript
//main.js
import {getName, getYear} from './helper';
getName()
```

## 写法5

```javascript
// export-default.js
export default function () {
  console.log('foo');
}
```

```javascript
// import-default.js
import getName from './export-default'
getName()
```


