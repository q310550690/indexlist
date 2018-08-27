# indexlist
工作中用到了indexlist 的需求，可官方不知道什么时候才移植这个插件，所以自己写了个，有问题欢迎反馈

## 使用方法
首先引入组件，然后在template里面使用，传入值和填写回调行数就行

## 组件接受的值
``` iscull ``` 是否需要转换数据格式 布尔值
```javascript
iscull
// <indexlist :iscull="true"></indexlist>
//标准格式是 {A:{...},B:{...}} 非标准格式是指 [{...},{....}] , 请看好数据格式，格式不对会报错
``` 

``` showtext ``` 在组件中显示的字段名 字符串
```javascript
showtext
// <indexlist :iscull="true" :showtext="'name'"></indexlist>
// 列 数据格式为 [{name:'你好',pinyin:'nh'}] indexlist就会显示你好
``` 

``` py ``` 在组件中搜索用的拼音首字母的字段名 字符串
```javascript
py
// <indexlist :iscull="true" :py="'pinyin'"></indexlist>
// 列 数据格式为 [{name:'你好',pinyin:'nh'}] 
``` 

``` title ``` 组件中显示的标题 字符串
```javascript
title
// <indexlist :title="'显示的标题'"></indexlist>
``` 

``` list ``` 数据 object
```javascript
list
// <indexlist :list="data"></indexlist>
// 标准格式是 data:{A:{...},B:{...}} 非标准格式是指 data:[{...},{....}]
// 只支持标准格式和非标准格式，否则报错
``` 

## 回调
``` result ``` 回调方法 function
```javascript
result
// <indexlist @result="resultFn"></indexlist>
// methods:{resultFn(e){console.log(e)}}
// 
``` 

## 组件方法
``` show() ``` 显示indexlist组件 function
```javascript
show()
// <indexlist @result="resultFn" ref="indexlist"></indexlist>
// methods:{showIndexList(e){this.$refs.indexlist.show();}
// 
``` 

``` hide() ``` 隐藏indexlist组件 function
```javascript
hide()
// <indexlist @result="resultFn" ref="indexlist"></indexlist>
// methods:{hideIndexList(e){this.$refs.indexlist.hide();}
// 
``` 

## 截图
[![PqRWGD.png](https://s1.ax1x.com/2018/08/27/PqRWGD.png)](https://imgchr.com/i/PqRWGD)
[![PqRhxH.png](https://s1.ax1x.com/2018/08/27/PqRhxH.png)](https://imgchr.com/i/PqRhxH)
[![PqRfRe.png](https://s1.ax1x.com/2018/08/27/PqRfRe.png)](https://imgchr.com/i/PqRfRe)
[![PqRRPO.png](https://s1.ax1x.com/2018/08/27/PqRRPO.png)](https://imgchr.com/i/PqRRPO)