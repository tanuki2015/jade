## 链接css的写法：

`link(rel="stylesheet" type="text/css” href="../bower_components/bootstrap/dist/css/bootstrap.css”)`

## 链接js

`script(type="text/javascript" src="../bower_components/jquery/dist/jquery.js")`

一个jade的骨架：
（引用的文件都是以编译后的位置来作参考）
```
doctype html
html
  head
    meta(charset="utf-8")
    link(rel="stylesheet" type="text/css" href="../bower_components/bootstrap/dist/css/bootstrap.css")
    title learn jade
  body
    .container.alert.alert-info
      h1 hello jade world
    script(type="text/javascript" src="../bower_components/jquery/dist/jquery.js")
    script(type="text/javascript" src="../bower_components/bootstrap/dist/js/bootstrap.js”)
```

本页面外层的文件是为了测试jade block的用法，dist目录中的文件是编译后的bootstrap的练习，源文件是bindex.jade.

## bootstrap基础
### 栅格参数,根据屏幕大小，只有一种生效
- xs extra small  <768px
- sm small        >=768px
- md middle       >=992px
- lg large        >=1170px

### 位置排列, push往右推，pull往左拉
下面调换两个div的显示位置，但html中的位置不变
.col-md-9
.col-md-3

- col-md-push-3
- col-md-pull-9

#### 不同屏幕大小条件下显示或隐藏
.visible-xs
.hidden-md

### 导航条
使用nav元素，navbar 和 navbar-default
```
nav(.navbar.navbar-default) // 导航条

ul.nav.navbar-nav // 导航条 中的 导航栏

nav.navbar.navbar-default
  a.navbar-brand(href="http://www.baidu.com")百度
  ul.nav.navbar-nav
    li.active
      a(href="#") A link
    li
      a(href="#") B link
    li
      a(href="#") C link
```

navbar-fixed-top 固定在顶部，button也行。

可以在页面中的style中重写这些类样式，或者引入自定义的时候放在bootstrap的css后面就行。

### 要使内容居中，只需要用.container包起来

### 导航条中的表单
- role属性是给bootstrap用的，便于准确渲染。
- .navbar-form表示是导航条中的表单，navbar-left表示定位在left
- .form-control是每一个输入项（input）都有的类
- glyphicon的图标放在空span中
```
form.navbar-form.navbar-left(action="post" role="form")
  input.form-control(type="text" placeholder="search")
  button(type="submit")
    span.glyphicon.glyphicon-search
```
