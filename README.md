![Rust中文](https://raw.githubusercontent.com/rustlang-cn/Important/master/files/rustlang-cn-small.png)

# Ruster  [![Build Status](https://travis-ci.org/rustlang-cn/ruster.svg?branch=master)](https://travis-ci.org/rustlang-cn/ruster)

online community in rust for rust community

## 架构实现：单页全栈 webapp，使用 Rust/actix-web 和 vuejs 完成。

- Async stable Actix-web framework/ 异步stable的 Actix-web框架

- diesel, postgresql r2d2/ diesel ORM框架、postgresql 10数据库、r2d2连接池

- SPA CORS JWT / 单页PWA、CORS、和JWT登陆

- Vuejs / Vuejs与vue-cli 3.0实现前端

## Ruster功能： 目前三大功能

1. 论坛：板块有：最美/博客/分享/问答/招聘/未回复 (论坛具有扩展性模块支持一键添加)

2. 博客：博客具有独立页面展示，具有收藏/喜欢属性，具有强大的热榜功能，最美模块分别根据最近一段时间内收藏量排行和全站收藏量2个排行榜，同时侧边栏根据收藏量展示最美的人排行榜

3. 文档：文档功能是具有自定义的html页面，可以不断添加海量wiki信息.

## 其他：

- 可视化与markdown二合一编辑器

- 丰富的个人中心

## How To

    first create a name 'ruster' postgresql database and a `dbuser` database account for this project. You should assure the `dbuser` is able to  use `ruster`. 

## when development/开发

```bash
$ git clone https://github.com/rustlang-cn/ruster.git
$ cd ruster
$ cargo install diesel_cli --no-default-features --features postgres
$ diesel setup
$ cargo run

// another shell nodejs(v10.1.0 on my machine)

$ cd ruster/webapp
$ npm install
$ npm run serve
```

then open browser 'http://localhost:8080'

## when production/生产

```bash
$ git clone https://github.com/rustlang-cn/ruster.git
$ cd ruster
$ cargo install diesel_cli --no-default-features --features postgres
$ diesel setup
$ cd webapp
$ npm install
$ npm run build
$ cd ..
$ cargo run --release
```

then open broswer 'http://localhost:8000/'

## 部署

```bash
$ git clone https://github.com/rustlang-cn/ruster.git
$ cd ruster
$ cargo install diesel_cli --no-default-features --features postgres
$ diesel setup
$ cd webapp
$ npm install
$ npm run build          // 在root目录生成`pubilc`静态文件目录
$ cd ..
$ cargo build --release  // 在root/target目录生成二进制文件 `ruster`
```

只需要将`二进制文件`(`target/release`目录下的`ruster`)和`pubilc`一起放在任意同一目录下，然后`./ruster`

## Screen

<img alt="Home" width="900" src="https://raw.githubusercontent.com/rustlang-cn/ruster/master/rust-cn.png">

## License

License is [here](https://github.com/rustlang-cn/ruster/blob/master/LICENSE)

Copyright (c) 2018-present, Xiangfei Wang
