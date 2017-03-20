# 移动框架与组件

[https://wisedu.github.io/bh-mint-ui2-doc/\#!/zh-cn2](https://wisedu.github.io/bh-mint-ui2-doc/#!/zh-cn2)

说明: 本文档用于指导前端 H5 App 的开发，如需开发其他其他功能组件比如小卡片等，不适用本文档

## 0. 前期准备:

1. Vue 的基本概念vue 文档  
2. es6 开发基本知识es6 基本文档  
3. Node 环境\(Node &gt;=4.0.0, npm &gt;= 3.0.0\)下载地址4. window 的 zip 环境  
   1. 移动门户 App[https://www.pgyer.com/VGkN](https://www.pgyer.com/VGkN)

## 1. 搭建脚手架

### 1.1 安装脚手架工具

打开命令行界面，首先检查有没有 npm 命令 检查方法

如果无法正常出现版本号，请去完成前期准备的第二步，安装 Node 和 NPM 环境 通过 npm 安装 vue 脚手架命令行工具

```
npm i -g vue-cli --registry=https://registry.npm.taobao.org

npm run dev
```

退出命令行，重新进入，检查有没有安装成功

如果没有正确弹出版本号，请尝试用管理员身份启动命令行或者 rtx 联系孙正斌

### 1.2 初始化脚手架

```
$ vue init wisedu/bh-mobile-template ${your_project}
```

命令会在当前的文件夹下生成一个文件夹，这个文件夹就是我们的项目文件夹

## 2. 运行项目

```
进入上一步创建的文件夹，运行命令
```

命令运行后，会去下载相关的依赖, 然后启动项目 项目启动在8080端口上，如果希望项目启动在，其他端口上，请修改 webpack.config.js顶部的 PORT

项目启动后，可以在浏览器里输入127.0.0.1:8080 或者 自己指定的端口，可以出现一个基本的页面

可以通过chrome 开发者工具，模拟出手机的屏幕方便开发

1. 项目基本结构

3.1 目录说明/doc

```
放置项目的文档，包括后端文档，设计文档等，方便多人开发这个项目的时候共享文档
```

/sr

```
项目源代码，开发人员编写的源代码都在这个目录下
```

/src/components

components 页面级别的公用组件, 例如在某个项目里共同使用的用户信息展示, 某些共用的复杂弹窗等等

/src/pages

pages 业务模块文件夹, 按照业务逻辑区分的业务模块文件夹

/src/vuex

vuex 用于放置 vuex 相关的文件\(mutation, store, action, getter\)

vuex 用于放置 vuex 相关的文件\(mutation, store, action, getter\)

3.2 目录规范

1. pages 目录下有一个业务建一个子文件夹, 文件夹以驼峰命名, 业务的主入口文件与文件夹名相同\(避免 sourceMap 无法区别文件问题\), 其他文件也以驼峰命名

2. components 目录下也分别建子文件夹, 文件夹以驼峰命名, 业务的主入口文件与文件夹名相同\(避免 sourceMap 无法区别文件问题\), 其他文件也以驼峰命名

3. vuex 目录下的命名规范见下文

vuex 命名规范

vuex 涉及的概念比较多 \(mutation, store, action, getter\), 文件和文件夹命名依旧驼峰

1. store.js 用于暴露最终的 store 对象

2. action.js 用于集合所有的 action

3. mutation 和 store 为了防止出现歧义, 原则上都必须分模块, 即使页面只有一个 vuex 的模块, 也需要在 vuex/module

   目录下建立一个独立的文件存放 相应的 mutation 和 store

4. 组件相关

资料:

移动端组件通过 npm，安装升级和使用，脚手架已经内置了组件的依赖，项目中如果需要使用组件请遵循以下流程，或组件文档

4.1 组件引入方法

在需要使用组件的\*.vue页面，通过 ES6 的 import 语法，引入组件，并在 component 区域注册需要用到的组件

1.官网  
2.文档地址  
3.demo 示例  
4. 扫码查看组件示例

```
具体的使用方法，可以参考附件中的示例代码
```

4.2 组件使用方法

请参考组件的文档地址

1. Hybrid SDK 相关5.1 介绍

Hybrid SDK 是前端应用调用客户端原生能力的桥梁，是对原生能力的封装，比如你想调起原生的图片浏览器，新开一个 webview 页面，设置原生的头，隐藏原生的头等，都会涉及到 Hybrid SDK

5.2 SDK 引入方法

在应用中可以通过全局变量 WISEDU\_SDK 取到Hybrid SDK 的上下文，这个时候，可以通过这个变量调用不同的 Hybrid 接口 比如，希望调用图片预览器就调用 WISEDU\_SDK.UI.preViewImages 来唤起原生的图片浏览器

5.3 SDK 文档

如果想了解具体有哪些 SDK 可以调用，需要的参数，请查看SDK 文档

1. 代码调试

请开发 App 的负责人和后端沟通解决跨域的问题，否则调试只能在 pc 浏览器的 chrome 下进行，其他真机或者手机浏览器调试都不行

6.1 pc 浏览器调试

chrome 打开开发者工具，点击模拟手机，即可调试应用

```
npm run
deploy
```

如果服务端不支持跨域，需要打开浏览器时禁掉跨域  
 mac: open -a "Google Chrome" --args --disable-web-security --user-data-dir windows:[http://stackoverflow.com/a/34779264/1433270需要先完全退出浏览器再使用才可生效](http://stackoverflow.com/a/34779264/1433270需要先完全退出浏览器再使用才可生效)

6.2 手机浏览器

直接使用手机浏览器访问，本机 ip:端口，然后Android 可以借助远程 debug 工具调试手机网页[http://wiki.jikexueyuan.com/project/chrome-](http://wiki.jikexueyuan.com/project/chrome-) devtools/remote-debugging-on-android.html

ios 可以利用 safari 进行调试

1. 在iOS设备上打开允许调试:设置→Safari→高级→打开”web检查器“

2. 在MAC上打开Safari的开发菜单:顶部菜单栏“Safari”→偏好设置→高级→打开”在菜单栏中显示“开发”菜单

3. 在iOS设备上的Safari浏览器中打开要调试的页面，然后切换到MAC的Safari，在顶部菜单栏选择“开发”→找到你的iOS设备名称→右边

   二级菜单选择需要调试的对应标签页，即可开始远程调试\(示意图\)

4. 如果没有iOS设备，也可以在Xcode中模拟一台，点击顶部“Xcode”→“Open Developer Tool”→“iOS

   Simulator”即可打开一个iOS设备的模拟器，并且模拟器里面Safari打开的页面，也是能通过上个步骤中MAC上的Safari调试。 \(示意图\)

6.3 应用内真机调试

1. Android 下载开发版的移动门户可以实现和6.2一样的远程调试 webview[https://www.pgyer.com/go1G](https://www.pgyer.com/go1G)

2. 开发者可以让测试人员在应用管理平台建立一个测试 App，在应用管理平台上你将该应用的 ip 指向你本地, 这时候你就可以在 app

   内调试你开发的小应用了

3. 打包上线

```
应用开发完成后，需要打包上线，框架层面提供命令打包
```

这个命令会在项目目录下生成一个 zip 包，zip 包的名字就是在初始化项目脚手架的时候询问的名字，这个 zip 交给项目负责任，或者放在服务器端已以 H5的形式发布或者放入应用管理平台以 Hybrid 形式发布
