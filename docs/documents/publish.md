# 打包发布

在开始之前，提一下两种重要的概念。带JSX的页面组件与通用组件，它们分别放在pages与components目录下，它们具有巨大的转换成本（毕竟JSX会被提取出来转换成wxml, axml, swan或ux文件），还有一种不带JSX的纯JS文件，建议放在common目录,  当然还有一些通用的东西可以通过npm安装，但不要使用那些有JSX的第三方依赖。


开发目录如下
```jsx
src
   |--components
   |    |--HotelDialog
   |    |--HotelXXX
   |    |--FlightYYY
   |    └── ...
   |--pages
   |    |--hotel
   |    |--flight
   |    |--holiday
   |    |--strategy
   |    └── ...
   |--common
   |    |--hotel
   |    |--flight
   |    |--holiday
   |    |--strategy
   |    └── ...
   |--app.js
```
components目录下为了扁平化管理，以事业部做前端+组件名的方式定义组子目录，目录下面就是index.js, index.scss或index.less。index.js里面必须是React组件，需要显式引入｀import React from "@react"`

>components目录下不要使用Fragments来命名子目录，这留给系统用。

pages目录下每个事业部各建一个目录，以事件部的名字命名，里面为index.js 及页面的目录，index.js要引入自己目录的所有页面，页面也以index.js命名，并且里面必须是有状态的React组件（转译器会转换成页面组件。）页面的index.js各种引入通用组件与common目录的依赖
```jsx
   |--pages
   |    |--hotel
            |--index.js //目录, import里面所有index.js
            |--page1
            |    |---index.js
            |    └── index.scss
            |--page2
            |    |---index.js
            |    └── index.scss
            |--page3
            |    |---index.js
            |    └── index.scss
            |--about
            |    |---index.js
            |    └── index.scss
```

common目录下每个事业部各建一个目录，以事件部的名字命名，里面为各种JS文件，它们只是纯业务逻辑，没有JSX，只会经过es67的语法糖转换。

app.js会引入pages每个事件的index.js, 只要稍微分析就得到整个应用全部有效的页面，放到app.json的pages数组中，或快应用的manifest.json的router对象的pages对象中
