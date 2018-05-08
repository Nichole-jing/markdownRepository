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
    
 #### 字符串的扩展
   * `codePointAt`方法是测试一个字符由两个字节还是由四个字节组成的最简单方法
   
    let s = '𠮷a';
    for (let ch of s) {
      console.log(ch.codePointAt(0).toString(16));
    }
   * 模板字符串
      * 优势：
      
        `链接：https://www.zhihu.com/question/21893022/answer/19647087`
        
            模板最本质的作用是【变静为动】一切利用这方面的都是优势，
            不利于的都是劣势。要很好地实现【变静为动】的目的，有这么几点：
            可维护性（后期改起来方便）；
            可扩展性（想要增加功能，增加需求方便）；
            开发效率提高（程序逻辑组织更好，调试方便）；
            看起来舒服（不容易写错）；
            从以上四点，你仔细想想，
            前端模板是不是无论从哪方便优势体现都不是一点两点。
            其实最重要的一点就是：【视图（包括展示渲染逻辑）与程序逻辑的分离】
       * 变量放在`${}`中$(变量)
   * 模板变异
   
       * 该模板使用`<%...%>`放置 JavaScript 代码，
       使用<%= ... %>输出 JavaScript 表达式
       
             let template = `
             <ul>
              <% for(let i=0; i < data.supplies.length; i++) { %>
                <li><%= data.supplies[i] %></li>
              <% } %>
             </ul>
             `;
 #### 数值的扩展 
   * Math.trunc 方法用于去除一个数的小数部分，返回整数部分。
        
        对于没有部署这个方法的环境，可以用下面的代码模拟。

         Math.trunc = Math.trunc || function(x) {
            return x < 0 ? Math.ceil(x) : Math.floor(x);
         };
 #### 函数的扩展
 