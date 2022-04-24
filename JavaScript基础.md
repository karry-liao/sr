1. **如何获取浏览器URL中查询字符串中的参数？**

   ```js
   //基础版本
   function getQueryString() {
       var sHref = window.loacation.href;
       var args = sHref.split("?");
       if(args[0] == sHref) {
           return "";
       }
       var arr = args[1].split("&");
       var obj = {};
       for (var i = 0; i < arr.length; i++){
           var arg = arr[i].split("=");
           obj[args[0]] = arg[1]
       }
       return obj;
   }
   var href = getQueryString();
   console.log(href["categoryId"]);
   
   //正则版本
   function getQueryString(name) {
       if(!name) return null;
       var after = window.location.search;
       after = after.substr(1) || window.location.hash.split("?")[1];
       if(!after) return null;
       if(after.index(name) === -1) return null;
       var reg = new RegExg("(^|&)" + name + "=([^&]*)(&|$)")
       var r = decordeURI(after).match(reg);
       if (!r) return null;
       return r[2];
   }
   cnosole.log(getQueryString("categoryId"));
   ```

2. **js实现一个打点计时器**

   **setTimeout方法**

   ```js
   function count(start,end) {
       if(start <= end) {
           console.log(start++);
           st = setTimeout(function() {
               count(start, end);
           },100);
       }
       return {
           cancel: function() {
               clearTimeout(st);
           }
       }
   }
   count(1,10)
   ```

   **setInterval()****方法**

   ```js
   function count(start, end){
       console.log(start++);
       var timer = setInterval(function() {
           if(start <= end) {
               console.log(start++);
           }
       },100);
       return {
           cancel: function(){
               clearInterval(timer);
           }
       }
   }
   count(1, 10);
   ```

   

3. **用js实现一个标砖的排序算法**

   **冒泡排序**

   ```js
   function BubbleSort(array) {
       var length = array.length;
       for (var i = length -1; i>0; i--) {
           for (var i = 0 ; j < i; j++) {
               if (array[j] > array[j+1]) {
                   var temp = array[j];
                   array[j] = array[j+1]
                   array[j+1] = temp;
               }
           }
           console.log(array);
           console.log("=========================")
       }
       return arry
   }
   var arr = [10,7, 6, 5, 11, 9, 8, 7, 3]
   var result = BubbleSort(arr);
   cnosole.log(result);
   ```

   

4. **正则表达式，验证手机号，验证规则：11位数字，以1开头**

5. **请给 Array 本地对象增加一个原型方法，用于删除数组中重复的条目并按升序排序，返回值是被删除条目的新数组**

​	

