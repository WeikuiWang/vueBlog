# vueBlog
使用vue+spring boot搭建的前后端分离博客项目。
涉及到的技术框架
* vue-cli
* element-ui
* spring-boot

#准备工作
> * [通过学习视频熟悉vue] (https://www.bilibili.com/video/BV1zi4y1w7UJ)    

> * 安装node.js

> * 配置idea开发vue环境
https://blog.csdn.net/u010026255/article/details/84581776

> * 全局安装安装webpack和webpack-cli
> &gt;npm install webpack -g
> &gt;npm install webpack webpack-cli -g
> &gt;webpack -v

> * 全局安装vue-cli
> &gt;npm install --global vue-cli

#1-项目开始
## 使用vue-cli脚手架创建项目
进入自己想要保存的项目目录，初始化项目和各个配置，其中eslint校验不用打开，其对空格和换行的校验令人抓狂。
> &gt;vue init webpack vueBlog
图片

进入项目vueBlog
> &gt;npm install

启动项目
> &gt;npm run dev

``` bash
>npm run dev
npm run dev
```
启动成功就可以本地http://localhost:8080访问初始的vue前端项目了。

#2-整合element ui/搭建登录页/解决跨域问题

安装vue-router,前面初始化项目时没有选择，这里手动安装是为了熟悉流程。
> &gt;npm install vue-router --save

整合element-ui
> &gt;npm i element-ui -S

