# 原子组件

### jsdoc文档

##### 1.0文档
http://res.wisedu.com/examples/components-v1/docs/bh_doc/1.0/

##### 1.2文档
http://res.wisedu.com/examples/components-v1/docs/bh_doc/1.2/

### 如何获取

通过以下两种方式都可以使用原子组件

##### 在页面引用

```html
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont/iconfont.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/iconfont_2.0/iconfont.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh.min.css">
<link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/jqwidget/blue/bh-scenes.min.css">
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bh_utils.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/jqwidget/jqxwidget.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bhtc/moment/min/moment-with-locales.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/bh.min.js"></script>
<script type="text/javascript" src="http://res.wisedu.com/fe_components/emap.js"></script>
```

##### 使用ubase集成

index.html

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="renderer" content="webkit">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <link type="text/css" rel="stylesheet" href="http://res.wisedu.com/fe_components/prism/prism.css">
    <!-- commomlib include jquery.js jquery.nicescroll.js jquery.fileupload.js director.min.js hogan.min.js lodash.min.js globalize.js-->
    <script src="http://res.wisedu.com/fe_components/commonlib.js"></script>
    <!-- 此处可以放置第三方库-->
    <script src="http://res.wisedu.com/fe_components/prism/prism.js"></script>
    <script src="http://res.wisedu.com/fe_components/appcore.js"></script>
</head>
<body>
</body>
</html>
```

## 调用组件

大部分通用组件我们引用了jQwidget，其官方帮助文档：[http://www.jqwidgets.com/jquery-widgets-demo/](http://www.jqwidgets.com/jquery-widgets-demo/)

考虑性能，我们对包尺寸有所缩减，我们仅包括了使用频率较高

| 组件名 | 组件名 | 组件名 |
| :--- | :--- | :--- |
| jqxButtons | jqxCalendar | jqxInput |
| jqxComboBox | jqxDateTimeInput | jqxDataAdapter |
| jqxDropDownList | jqxListBox | jqxLoader |
| jqxMenu | jqxNotification | jqxNumberInput |
| jqxPanel | jqxPopOver | jqxScrollBar |
| jqxTabs | jqxTextArea | jqxTooltip |
| jqxTree | jqxValidator | jqxWindow |
| jqxProgressBar | jqxNavigationBar | jqxDragDrop |

<mark>更多组件我们采用了三方插件 和 我们的特色组件（bh组件）</mark>

**请参考本章节下面的每个组件示例**

