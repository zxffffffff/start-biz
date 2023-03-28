# Kubernetes(K8s)

## 资料
- 文档: https://kubernetes.io/zh-cn/docs/home/
- 源码: https://github.com/kubernetes/kubernetes

## 简介
- 用于自动部署、扩缩和管理容器化应用程序的开源系统，通常与 Docker 一起使用
- Google 开源, Apache-2.0 license, Go

## 学习安装 minikube
- https://kubernetes.io/zh-cn/docs/tasks/tools/
- 提示：安装 Docker Desktop 可能自带 kubectl
- 检查 kubectl: `kubectl version --client --output=yaml`
- 管理员运行 minikube: `minikube start` (虚拟机需要4G内存)
- [todo] 

## 生产安装 kubeadm
- https://kubernetes.io/zh-cn/docs/setup/production-environment/tools/kubeadm/install-kubeadm/
- 生产环境: Linux 至少 2 Cores 2GB RAM
- [todo] 运行

