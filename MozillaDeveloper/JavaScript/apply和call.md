apply与call的区别
=====
###apply(obj,arguments)
    obj:是调用者的this指引
    arguments:是一个参数数组
###call(obj,param1,...)
    obj:是调用者的this指引
    param1:是参数列表，多个参数以逗号隔开
####apply中要求是一个参数数组，而call是参数列表
####我们可以利用这个特性来计算数组的极值问题和两个数组的合并，下面为给出的示例代码
###最大值示例代码：
  ```js
  var array = [1,2,3,4,5];
  var max=Math.max.apply(null,array);//这里的null表示没有对象去调用它，我们只需要返回数组中的最大值而已。
  ```
### Array.prototype.push 可以实现两个数组合并
```js
vararr1=new Array("1","2","3");  
vararr2=new Array("4","5","6");  
Array.prototype.push.apply(arr1,arr2);  
```
