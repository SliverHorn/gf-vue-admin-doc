## 目录结构

###  web 目录结构

```bash
└─web
  ├── public
  └── src
      ├── api
      ├── assets
      ├── components
      ├── directive
      ├── router
      ├── store
      ├── style
      ├── utils
      └── view
```

### web 目录结构详解

| 目录/文件名称 | 说明                   | 描述 |
| :------------ | :--------------------- | :--- |
| public        | 发布模板               |      |
| src           | 源码包                 |      |
| - api         | 向后台发送ajax的封装层 |      |
| - assets      | 静态文件               |      |
| - components  | 组件                   |      |
| - router      | 前端路由               |      |
| - store       | vuex 状态管理仓        |      |
| - style       | 通用样式文件           |      |
| - utils       | 前端工具库             |      |
| - view        | 前端页面               |      |

### server 目录结构

```shell 
├── server
  ├── app
  │   ├── api
  │   │   ├── request
  │   │   ├── response
  │   │   └── v1
  │   ├── middleware
  │   ├── model
  │   └── service
  ├── boot
  ├── config
  ├── db
  ├── library
  │   ├── gdbadapter
  │   ├── global
  │   └── utils
  ├── logs
  │   ├── log
  │   ├── server
  │   └── sql
  ├── packed
  ├── public
  ├── router
  └── template
  ├── Dockerfile
  ├── go.mod
  └── main.go
```

### server 目录结构详解

| 目录/文件名称 | 说明         | 描述                                                         |
| :------------ | :----------- | :----------------------------------------------------------- |
| `app`         | 业务逻辑层   | 所有的业务逻辑存放目录。                                     |
| - `api`       | 业务接口     | 接收/解析用户输入参数的入口/接口层。                         |
| --`request`   | 入参结构体   | 接收前端发送到后端的数据。                                   |
| --`response`  | 出参结构体   | 返回给前端的数据结构体                                       |
| -- `v1`       | api层        | api层v1版本代码                                              |
| -`middleware` | 中间件       | 用于路由层的中间件存放文件夹                                 |
| - `model`     | 数据模型     | 数据管理层，仅用于操作管理数据，如数据库操作。               |
| - `service`   | 逻辑封装     | 业务逻辑封装层，实现特定的业务需求，可供不同的包调用。       |
| `boot`        | 初始化包     | 用于项目初始化参数设置，往往作为`main.go`中第一个被`import`的包。 |
| `config`      | 配置管理     | 所有的配置文件存放目录。                                     |
| `db`          | 初始数据     | 存放项目的初始数据                                           |
| `library`     | 公共库包     | 公共的功能封装包，往往不包含业务需求实现。                   |
| -`gdbadapter` | gdb适配器    | GoFrame适配器工具类                                          |
| -`global`     | json返回封装 | json返回web端的统一封装                                      |
| - `utils`     | 工具类       | 一些常用的工具类封装                                         |
| `logs`        | glog日志     | glog会自行判断是否存在此目录,无会自动创建                    |
| -`log`        | 普通日志     | 普通日志                                                     |
| -`server`     | 服务器日志   | server日志                                                   |
| -`sql`        | 数据库日志   | 存放mysql产生log的sql日志                                    |
| `packed`      | 打包目录     | 将资源文件打包的`Go`文件存放在这里，`boot`包初始化时会自动调用。 |
| `public`      | 静态目录     | 仅有该目录下的文件才能对外提供静态服务访问。                 |
| `router`      | 路由注册     | 用于路由统一的注册管理。                                     |
| `template`    | 模板文件     | 存放自动化代码渲染模板                                       |
| `Dockerfile`  | 镜像描述     | 云原生时代用于编译生成Docker镜像的描述文件。                 |
| `go.mod`      | 依赖管理     | 使用`Go Module`包管理的依赖描述文件。                        |
| `main.go`     | 入口文件     | 程序入口文件。                                               |