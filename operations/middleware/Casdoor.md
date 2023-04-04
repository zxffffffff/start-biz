# Casdoor 
统一身份认证系统（注册、登陆、会话、权限）

## 简介
- 源码：https://github.com/casdoor/casdoor
- 文档：https://casdoor.org
- 在线 Demo：https://casdoor.org
- Apache-2.0 license, Go
- 一个集中认证/单点登录(SSO) 平台，前端是React，并提供了各语言 client-sdk

## 部署
- https://casdoor.org/zh/docs/basic/try-with-docker
- docker 部署测试，自带 MySQL（casdoor-all-in-one）
```docker
# http://localhost:8000 admin 123
docker run -p 8000:8000 casbin/casdoor-all-in-one
```
- docker 部署生产，连接 MySQL（casdoor）
```docker
# 创建 conf/app.conf文件
docker run -e driverName=mysql -e dataSourceName='user:password@tcp(x.x.x.x:3306)/' -p 8000:8000 casbin/casdoor:latest
```

