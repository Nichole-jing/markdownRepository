###  ECMAScript6
 #### 变量的解析赋值 
 `如果解构不成功，变量的值就等于undefined。` 
   * 模式匹配 
     > let [a, b, c] = [1, 2, 3];
      * 嵌套赋值
      
      
         let [foo, [[bar], baz]] = [1, [[2], 3]];
         foo // 1
         bar // 2
         baz // 3
         let [head, ...tail] = [1, 2, 3, 4];
         head // 1
         tail // [2, 3, 4]
   > 注意，ES6 内部使用严格相等运算符（===），
   判断一个位置是否有值。所以，只有当一个数组成员严格等于undefined，
   默认值才会生效。
   
   * 对象的解构
         
    数组的元素是按次序排列的，变量的取值由它的位置决定；
    而对象的属性没有次序，变量必须与属性同名，才能取到正确的值。
    let { foo: baz } = { foo: "aaa", bar: "bbb" };
    baz // "aaa"
    foo // error: foo is not defined