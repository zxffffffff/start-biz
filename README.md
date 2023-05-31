# start-biz
一个快速展业的微服务脚手架，支持各类云服务 SaaS PaaS FaaS

## 结构
![image](https://github.com/zxffffffff/start-biz/blob/main/doc/Architecture.png)

## 目标
- 快速搭建(脚手架、脚本、配置文件、...)
- 方便扩展支持各个云原生厂商(阿里云、华为云、AWS、...)
- 云计算部分支持移植到 FaaS

## 思考
- 小规模应用不适合搞得太复杂，第三方服务使用 Docker 部署即可，本地服务越简单部署越好
- 如果应用数量很多，使用 K8s 能提高运维效率



# 开发(development)

## API网关(API-Gateway)
- [todo] Ingress: 流量入口负载均衡，支持 K8s

## 微服务(microservice)
- C++
- Java
- Go
- [todo] Node.js
- [todo] Python

## 客户端(client)
- [todo] multi-platform
- Electron(Node.js)
- Flutter(Dart)
- Flame(Flutter)
- Godot(C++/GDScript)



# 运维(operations)

## 容器(container)
- [WIP] Docker
- [WIP] Kubernetes(K8s)

## 数据库(DB)
- [WIP] MySQL
- [WIP] PostgreSQL
- [todo] MongoDB
- [todo] Redis
- [todo] 对象存储
- [todo] 表单存储

## 中间件(middleware)
- [todo] Dubbo: 远程调用，支持 gRPC
- [todo] Nacos: 注册中心、配置中心
- [WIP] Keycloak/Casdoor: 用户身份管理、权限控制
- [todo] Jena: 用于处理和管理RDF数据和Linked Data



# DevOps

## 版本控制(code version)
- [todo] GitLab
- [todo] 分支管理: dev，feature，release

## 持续集成/持续交付(CI/CD)
- [todo] 自动化测试(auto test)
- [todo] 代码审查(code review)
- [todo] 灰度发布(金丝雀发布，蓝绿发布，A/B测试)
- [todo] Jenkins: 自动化打包平台
- [WIP] Node-RED：低码平台

