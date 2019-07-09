[原教程地址](https://learnku.com/articles/9054/laravel55-vue-development-single-page-application)

环境为laradock,请自行安装

`composer create-project laravel/laravel vue 5.5.* --prefer-dist`下载laravel框架

更改nginx配置文件`laradock/nginx/sites/default.conf`，指向新建的`vue/public`目录

`docker-compose build nginx` 更新nginx配置

`docker-compose up -d nginx mysql` 开启容器

_**注意：laravel框架里的evn文件中，DB_HOST一项不能填写localhost或者127.0.0.1，我写的是自己的局域网ip地址，教程上说也可以写mysql**_

然后，根据[教程](https://learnku.com/articles/9054/laravel55-vue-development-single-page-application)抄一下代码吧

最后,教程中缺少的部分:

`php artisan migrate` 创建完迁移文件后，别忘了迁移动作

**npm网速慢的，可以使用淘宝镜像[cnpm](https://npm.taobao.org/)**

`cnpm install vue-router --save-dev `安装vue-router

`cnpm install vuex --save-dev` 安装vuex