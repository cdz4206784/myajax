# Ajax 正常请求 GET demo4

``` bash
> document.getElementById("button").addEventListener("click",getData);
> function getData(){
>     var xhr = new XMLHttpRequest();
>     xhr.open("GET",'process.php?name=Henry',true);
>     xhr.onload = function(){
>         console.log(this.responseText);
>     }
>     xhr.send();
> }
```

# Ajax 请求数据 GET demo4
``` bash
> document.getElementById("getForm").addEventListener("submit",getForm);
> function getForm(e){
>     e.preventDefault();
>     var name = document.getElementById("name1").value;
>     var xhr = new XMLHttpRequest();
>     xhr.open("GET",'process.php?name='+name,true);
>     xhr.onload = function(){
>         console.log(this.responseText);
>     }
>     xhr.send();
> }
```

# Ajax 请求数据 POST demo4
``` bash
> document.getElementById("postForm").addEventListener("submit",postForm);
> function postForm(e){
>     e.preventDefault();
>     var name = document.getElementById("name2").value;
>     var params = "name="+name;
>     var xhr = new XMLHttpRequest();
>     xhr.open("POST",'process.php',true);
>     // 设置请求头
>     xhr.setRequestHeader('Content-type','application/x-www-form-urlencoded');
>     xhr.onload = function(){
>         console.log(this.responseText);
>     }
>     xhr.send(params);
> }
```

# 状态码
``` bash
// readyState 状态码
// 0: 请求未初始化
// 1: 服务器连接已建立
// 2：请求已接收
// 3：请求处理中
// 4：请示已完成，且响应已就绪

// HTTP 状态码
// 200 - 服务器成功返回网页
// 404 - 请求的网页不存在
// 503 - 服务器暂时不可用
```





