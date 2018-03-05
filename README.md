# 什么是Prometheus?

Prometheus是由SoundCloud开源监控告警解决方案, 从2012年开始编写代码, 再到2015年github上开源以来, 已经吸引了9k+关, 以及很多大公司的使用; 2016年Prometheus成为继k8s后, 第二名CNCF(Cloud Native Computing Foundation)成员。

## 主要功能

- 多维数据模型(时序由 metric名字和k/v的labels构成)。
- 灵活的查询语句(PromQL)。
- 无依赖存储, 支持local和remote不同模型。
- 采用http协议, 使用pull模式, 拉取数据, 简单易懂。
- 监控目标, 可以采用服务发现或静态配置的方式。
- 支持多种统计数据模型, 图形化友好。

## 基础架构

![](https://cdn.rawgit.com/prometheus/prometheus/c34257d069c630685da35bcef084632ffd5d6209/documentation/images/architecture.svg)

## Install
1. 创建`monitoring namespaece`
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-namespace.yaml
```

2. 创建`kube-state-metrics`服务的`Service Account`, `ClusterRole`, `Role`,
`ClusterRoleBinding`, and `RoleBinding`.
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/kube-state-metrics-rbac.yaml
```

3.部署`kube-state-metrics`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/kube-state-metrics-deployment.yaml
```

4. 部署`node-directory-size-metrics`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/node-directory-size-metrics.yaml

5. 创建`prometheus`服务的`Service Account`, `ClusterRole`, `Role`,
`ClusterRoleBinding`, and `RoleBinding`.
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-rbac.yaml
```

6. 创建`prometheus configmap`
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-configmap.yaml
```

7. 创建`prometheus`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-deployment.yaml
```

8. 部署`prometheus-node-exporter`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-node-exporter.yaml
```

9. 部署`prometheus ingress`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Prometheus/master/prometheus-ingress.yaml
```
