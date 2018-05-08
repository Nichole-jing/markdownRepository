* JavaScript中的数组遍历forEach()与map()方法以及兼容写法
* 字符串的长度值是指字符的数量
  * 对于字符串函数：left，right，其长度值是指字符的数量；
  * 对于含有位置参数的字符串函数，charindex、stuff 和 substring，是以字符数量来计算起始位置和长度。
* 开发中固定字体大小用rem的话，要给html写上字体大小：100pxrem（`font-size:100px`）,后续的字体大小除以100+`rem`
* for..of遍历用法：
    
   1.如果是es5 只能遍历数组元素
   
      var myArray=[1,2,4]
      myArray.name="数组";
      for (var value of myArray) {
         console.log(value);
      }
      输出：1,2,4
   2.如果是es6 遍历map
     
     1.map()遍历
        
      const map = new Map();
      map.set('first', 'hello');
      map.set('second', 'world');
   
      for (let [key, value] of map) {
          console.log(key + " is " + value);
      }
      输出：first is hello
      second is world 
      // 获取键名
      for (let [key] of map) {
        console.log(key）
      }
      输出：first，second
      // 获取键值
      for (let [value] of map) {
        console.log(value）
      }
      输出：hello，world 
    
    2.字符串的遍历 
* ECMAScript Function 对象（类）
    * new function()
    
* evel.call()
* echo()方法
* alert缺点：阻止浏览器的所有动作
* eslink 本身不具备检测代码功能 （ide高级的话 会自动检测），要用的话需要写命令运行      