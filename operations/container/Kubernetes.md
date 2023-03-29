# Kubernetes(K8s)
K8s 重点在于服务编排，对于小规模的开发团队没有实际意义，Docker 部署足矣。

## 简介
- 文档: https://kubernetes.io/zh-cn/docs/home/
- 源码: https://github.com/kubernetes/kubernetes
- 用于自动部署、扩缩和管理容器化应用程序的开源系统
- Google 开源, Apache-2.0 license, Go

## 学习安装 minikube
- https://kubernetes.io/zh-cn/docs/tasks/tools/
- https://minikube.sigs.k8s.io/docs/start/
- 提示：安装 Docker Desktop 自带 kubectl
- 检查 kubectl: `kubectl version --client --output=yaml`
- 管理员运行 minikube: 
```sh
minikube start
minikube kubectl -- get po -A
minikube addons enable ingress # 建议启用 Ingress 插件
minikube dashboard # 跳转到 k8s 后台
```

## 生产部署 kubeadm
- https://kubernetes.io/zh-cn/docs/setup/production-environment/
- 生产环境: Linux 至少 2 Cores 2GB RAM

