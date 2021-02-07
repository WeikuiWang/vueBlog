# vueBlog
使用vue+spring boot搭建的前后端分离博客项目。
涉及到的技术框架
* vue-cli
* element-ui
* spring-boot
以下为实现过程中笔记记录：
# 准备工作
* [通过学习视频熟悉vue](https://www.bilibili.com/video/BV1zi4y1w7UJ)    

* 安装node.js

* [配置idea开发vue环境](https://blog.csdn.net/u010026255/article/details/84581776)

* 全局安装安装webpack和webpack-cli
``` bash
npm install webpack -g
npm install webpack webpack-cli -g
webpack -v
```
* 全局安装vue-cli
``` bash
npm install --global vue-cli
```

# 1-项目开始
使用vue-cli脚手架创建项目,进入自己想要保存的项目目录，初始化项目和各个配置，其中eslint校验不用打开，其对空格和换行的校验令人抓狂。
``` bash
vue init webpack vueBlog
```

进入项目vueBlog
``` bash
npm install
```
启动项目
``` bash
npm run dev
```

启动成功就可以本地http://localhost:8080访问初始的vue前端项目了。

# 2-整合element ui/搭建登录页/解决跨域问题

安装vue-router,前面初始化项目时没有选择，这里手动安装是为了熟悉流程。
``` bash
npm install vue-router --save
```

整合element-ui
``` bash
npm i element-ui -S
```

Todolist:

- [x] 搭建vue-cli项目，整合element-ui，创建管理后台登录页
- [ ] 搭建spring-boot后端项目，解决跨域问题，前后端接口实现交互
- [ ] 博客列表管理页设计与实现
- [ ] 标签列表管理设计与实现