# 类和继承
1. 构造函数

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log( `hello, ${this.name}, i am ${this.age} years old`);
  }
}
```

等价于

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

Person.prototype.sayHello = function () {
  console.log(  `hello, ${this.name}, i am ${this.age} years old`);
};

var p = new Person('hunger', 2);
```

2. 静态方法

```javascript
class EventCenter {
  static fire() {
    return 'fire';
  }
  static on(){
    return 'on'
  }
}
```

等同于

```javascript
function EventCenter(){
}
EventCenter.fire = function(){}
EventCenter.on = function(){}

```

3. 继承

```javascrit
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  sayHello() {
    console.log( `hello, ${this.name}, i am ${this.age} years old`);
  }
}
class Student extends Person {
  constructor(name, age, score) {
    super(name, age); 
    this.score = score;
  }

  sayScore() {
     console.log(  `hello, ${this.name}, i am ${this.age} years old, i get ${this.score}`);
  }
}
```



