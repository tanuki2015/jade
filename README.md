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

####不同屏幕大小条件下显示或隐藏
.visible-xs
.hidden-md
