# JavaScript 快速入门

## 基本语法

[JavaScript 基础](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/JavaScript_basics)

## 常用库

### 切片

JavaScript 通过切片模拟栈和队列

栈

```javascript
// 创建栈
function Stack(){
    var items = []; 
}
// push压入
this.push = function (element) {
    items.push(element);
}
// pop弹出
this.pop = function () {
    return items.pop();
}
// 检查栈空
this.isEmpty = function () {
    return items.length == 0;
}
```

队列

```javascript
// 创建队列
function Queue(){
    var items = [];
}
// enqueue入队
this.enqueue = function(element){
    items.push(element);
}
// dequeue出队
this.dequeue(){
    return items.shift();
}
// 长度0为空
this.isEmpty = function(){
    return items.length==0
}
```

注意点

- 默认 s=s[0:len(s)]，取下限不取上限，数学表示为：[)

### 字典

基本用法

```javascript
// 创建
let m = new Map();
// 设置kv
m.set('hello', 1);
// 删除k
m.delete('hello');
// 遍历
for(var key in m) {
  var value = m[key];
  console.log(key, value);
}
```

注意点

- Map 键可以是任何值 （包括函数、对象和任何基本类型）。
- 在Map中正确存储数据的方式是通过```set(key, value)```方法。


### 标准库

sort

```javascript
arr.sort([compareFunction])
```

math

```javascript
// 最大最小值
Number.MAX_SAFE_INTEGER // 实际值：2的53次方减一
Number.MIN_SAFE_INTEGER // 实际值：-2的53次方加一
```

## 刷题注意点

- leetcode 中，全局变量不要当做返回值，否则刷题检查器会报错
