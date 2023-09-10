# reactStudy
react学习
当下以及未来的前端开发一定是组件化【模块化】的开发
  有利于团队协作开发
  便于组件的复用，提交开发效率，方便后期维护、减少页面冗余代码

如何划分组件
  业务组件：针对项目需求
    普通业务组件: 没有啥复用性，只是单独拆出来的一个模块
    通用业务组件：具备复用性，
  功能组件：使用多个项目[UI组件库组件]
    通用功能组件
    

因为组件化开发，必然带来工程化处理
  基于webpack等打包工具【vite/turbopack/rollup】
   + 实现组件的合并、压缩、打包等
   + 代码编译、兼容处理、校验等
   + ....

=====react工程化组件化开发
1. create-react-app
  可以基于webpack纯手动搭建架子，但是这样麻烦
  react官方为大家提供一个脚手架【create-react-app】
  + 所谓的脚手架就是默认把webpack的打包规则已经配置好了，把一些项目需要的基本内容也都处理好了
1.1 基本使用
  安装脚手架

  基于脚手架创建react-app的项目
    create-react-app demo

  项目目录：
    |- node_modules
    |- src: 
      |- index.js
    |- public
      |- index.html
    |- package.json


1.2 结构分析
1.2.1 package.json
create-react-app会默认安装react、react-dom
  react【react的框架核心】
  react-dom【react视图渲染的核心、基于react构建webapp】

      为什么react要分成react和react-dom呢？
        因为react-native构建和渲染app的，react-dom是构建渲染html的
  react-script： 脚手架为了让项目文件看上去更整洁，把webpack打包规则、loader、相关插件都隐藏到的node_modules目录下
      react-script就是脚手架中自己对于打包命令的一种封装，基于它打包，会调用node_module下的 【看看执行的脚本，都是】

1.2.2 src[打包入口]
只留一个index.js 其他全删除

注意： react版本目前主要是16【用的比较多】、17【基本没有特点】、18版本【新版本，与16版本的差别还是蛮答】
