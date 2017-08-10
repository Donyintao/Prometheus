# 什么是Prometheus？

[![CircleCI](https://circleci.com/gh/prometheus/prometheus/tree/master.svg?style=shield)][circleci]
[![Docker Repository on Quay](https://quay.io/repository/prometheus/prometheus/status)][quay]
[![Docker Pulls](https://img.shields.io/docker/pulls/prom/prometheus.svg?maxAge=604800)][hub]
[![Go Report Card](https://goreportcard.com/badge/github.com/prometheus/prometheus)](https://goreportcard.com/report/github.com/prometheus/prometheus)
[![Code Climate](https://codeclimate.com/github/prometheus/prometheus/badges/gpa.svg)](https://codeclimate.com/github/prometheus/prometheus)
[![Issue Count](https://codeclimate.com/github/prometheus/prometheus/badges/issue_count.svg)](https://codeclimate.com/github/prometheus/prometheus)

Visit [prometheus.io](https://prometheus.io) for the full documentation,
examples and guides.

Prometheus 是由 SoundCloud 开源监控告警解决方案，从 2012 年开始编写代码，再到 2015 年 github 上开源以来，已经吸引了 9k+ 关注，以及很多大公司的使用；2016 年 Prometheus 成为继 k8s 后，第二名 CNCF(Cloud Native Computing Foundation) 成员。

# 主要功能:

- 多维数据模型(时序由 metric名字和k/v的labels构成).
- 灵活的查询语句(PromQL).
- 无依赖存储, 支持local和remote不同模型.
- 采用http协议, 使用pull模式, 拉取数据, 简单易懂.
- 监控目标, 可以采用服务发现或静态配置的方式.
- 支持多种统计数据模型, 图形化友好.

## 基础架构

![](https://cdn.rawgit.com/prometheus/prometheus/c34257d069c630685da35bcef084632ffd5d6209/documentation/images/architecture.svg)
