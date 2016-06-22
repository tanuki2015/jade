链接css的写法：

`link(rel="stylesheet" type="text/css” href="../bower_components/bootstrap/dist/css/bootstrap.css”)`

链接js

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
