# 自动化集成服务 -spb-ci

整合Docker、Jenkins、Gitlab，搭建企业持续集成服务，实现开发流程化、项目持续交付、自动化部署

优势
-----------

* 服务器资源和配置使用 [docker.volumes](https://docs.docker.com/engine/admin/volumes/volumes) 添加进容器，实现资源文件可备份、方便迁移

* 使用 [dockerfile](https://docs.docker.com/engine/reference/builder/)、[docker-compose](https://docs.docker.com/compose/overview/) 配置服务器，使服务可复制，方便部署和操作

安装使用
-----------

把项目clone到本地
```
git clone git@github.com:zygeilit/spb-ci.git
```

使用Docker创建镜像以及启动服务器
```
docker-compose up --build -d
```

创建并复制Gitlab的Persion Token到/mounts/gitlab-private-token
```
./cmd-init-credential.sh
```

先决条件
-----------

系统中安装了 Docker、Docker Compose，具体的安装步骤可见 [Docker官方文档](https://www.docker.com)
