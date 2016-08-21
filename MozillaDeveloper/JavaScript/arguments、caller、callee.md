##arguments
在函数调用时，函数会自动生成arguments对象，该对象包含传递过来的实参,一般可以用于获取实参个数以及实参值。
例如：
```js
function f1(){
  console.log(arguments.length);
}
f1(1,2,3,4);//在控制台会输出4
```
##caller
在一个函数被另一个函数调用时，被调用函数会生成一个caller对象，caller指向调用者的函数对象，如果未调用，则caller为null。
```js
function testCaller() {  
    var caller = testCaller.caller;  
    alert(caller);  
}  
function aCaller() {  
    testCaller();  
}  
  
aCaller();  
```
##callee
当函数被调用时，arguments.callee会指向自身，就是自己的引用，一般会用于递归。
```js
function sub(num){
  if(num > 0){
    num +=arguments.callee(num-1);
  }
  return num;
}
```
