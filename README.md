
# 过滤器(管道)
******
**这里讲到过滤器，现在我更愿意称它为[pipes](https://github.com/huich/Pipes/blob/master/items/pipe.md)(管道)。刚接触angular时，称它为过滤器，用来格式化数字(千分位)、日期、金额加￥，很方便。这也是我总结它的原因，总结的过程中看了官方文档，无论是angular还是vue,他们都提到了管道的概念，数据通过管道来转换格式，更方便理解了** 

#### 框架使用情况 :point_down:
|框架| angular | vue | react |
|:--------:|:--------:| :--------:|:--------:|
|pipes| :white_check_mark: | :white_check_mark: |:heavy_multiplication_x:|

* react没有pipe的概念并不代表他不能实现管道 :point_right:[参考](https://stackoverflow.com/questions/54668921/how-we-can-use-pipes-in-react-javascript/54668977)

******

## Angular-Pipes 
**AngularJS内置了很多过滤器，在HTML模板的绑定符号{{}}内通过｜来调用管道**  
 
1. 内置管道  
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
2.自定义管道 

******
## vue-filters
**可以在{{date|formatdate}}实现，或者使用'v-bind' ```<div v-bind:id="rawId | formatId"></div>```**
  
