# 过滤器(管道)
******
**这里讲到过滤器，现在我叫它[pipes](https://github.com/huich/Pipes/blob/master/items/pipe.md)(管道)。刚接触angular时，我叫它过滤器，用来格式化数字(千分位)、日期、金额加￥，很方便。这也是我总结它的原因，总结的过程中看了官方文档，无论是angular还是vue,他们叫过滤器为管道，数据通过管道来转换格式，更方便理解了**
## Angular-Pipes
### Angular-过滤器  
**AngularJS内置了很多过滤器，在HTML模板的绑定符号{{}}内通过｜来调用过滤器**  
目录  

1. 内置过滤器  
  * 字母转换成大写  
  * 数字转换千分位  
  * 日期格式化  
  * 数字格式化成货币  
  
2. 自定义过滤器  
******
1. 内置过滤器  
* 字母转换成大写 
```
$scope.pageData.Str="cheng";
{{pageData.Str|uppercase}}//输出==>CHENG
``` 
* 数字转换千分位 
```
$scope.pageData.Num=1000;
{{pageData.Num|number}}//输出==>1,000
``` 
* 日期格式转换 
```
$scope.pageData.Date=new Date();
{{pageData.Date|date:'yy-MM-dd'}}//输出==>2020-01-10
``` 
* 数字格式化成货币 
```
$scope.pageData.Money=1000;
{{pageData.Money|currency:'¥'}}//输出==>¥1,000.00
``` 
  
