### 手写promise

```javascript
var promise = new promise((resolve, reject) => {
    if(success) {
        resolve(value)
    } else {
        reject(error)
    }
});

promise.then(res => console.log(res))
	   .catch(err => {
    console.log(err)
});
```

### 解决函数回调里面回调另一个函数，另一个函数需要依赖这个回调函数的问题——使用promise async/await

```js
function awaitMethod(num){
    return new Promise((resolve,reject) => {
        setTimeout(() =>{
            resolve(num * 3);
        },2000);
    });
}
//!!!!!!!!!await 表示所有await语句都执行完成后才继续向下执行，await这个关键字只能在async定义的函数里面使用。
async function test(){
    let result =await awaitMethod(30);
    console.log(result);
    let next = await awaitMethod(result);
    console.log(next);
    return next;
}

test().then(success => cnosole.log('成功',success))
	  .catch(error => console.log("失败", error))
```