### for in遍历对象时，使用hasOwnProperty过滤掉原型链中的属性
```javascript
var newInfo={};
for(var key in info){
   if(info.hasOwnProperty(key)){
     newInfo[key]=info[key]
   }
}
```
tips:hasOwnProperty判断一个对象是否有名称的属性或对象，此方法无法检查该对象的原型链中是否具有该属性，该属性必须是对象本身的一个成员。 
如果该属性或者方法是 该对象 自身定义的 而不是 原型链 中定义的 则返回true;否则返回false;

### 对有序集合进行顺序无关的遍历时，使用逆序遍历。
解释：

逆序遍历可以节省变量，代码比较优化。
```javascript
var len = elements.length;
while (len--) {
    var element = elements[len];
    // ......
}
```