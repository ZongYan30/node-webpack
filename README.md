# 使用webpack搭建node应用

## 使用Node开发的两种方式

### 1.直接开发，直接部署

1. 搭建 node 工程，直接开发
2. 开发过程中使用 git 进行管理
3. 开发完成后，提交 git
4. 进入部署服务器，从 git 中拉取最新代码，然后`npm install`

**问题：**

1. 服务器在`npm install`的过程中，会占用比较大的网络资源
2. 代码没有压缩，拉取速度较慢
3. 开发过程中，无法使用较新的语法
4. 开发过程中，无法使用 ES6 模块化

## 2.直接开发，用 webpack 打包，然后部署

1. 搭建 node + webpack 工程
2. 开发后，使用 webpack 打包
3. 将打包结果上传到服务器，服务器直接运行

生产环境的运行：(**具体去看package.json的dev命令**)

1. 监控源代码目录，如果源代码有变动
2. 将环境变量设置为`development`，然后进行打包
3. 运行打包结果



**注意:webpack的配置文件需要设置`target:node`,因为默认的`web`是找不到node的内置模块的(fs等)**

## 模板地址

[node-webpack](https://github.com/ZongYan30/node-webpack)