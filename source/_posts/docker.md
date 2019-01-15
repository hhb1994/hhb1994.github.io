---
title: 熟悉 docker
tags: [docker]
categories: 知识 
---

# 什么是 docker?

![](http://www.ruanyifeng.com/blogimg/asset/2018/bg2018020901.png)
docker 属于 linux 容器的一种封装.

## 什么是 Linux 容器

Linux 容器不是模拟一个完整的操作系统，而是对进程进行隔离。或者说，在正常进程的外面套了一个保护层。对于容器里面的进程来说，它接触到的各种资源都是虚拟的，从而实现与底层系统的隔离。

由于容器是进程级别的，相比虚拟机有启动快,资源占用少,体积小的优势.

# docker 的用途

* 提供一次性的环境;
* 提供弹性的云服务;
* 组建微服务架构.

# docker 的架构

![](https://static.oschina.net/uploads/space/2017/0705/154125_8LwL_1251444.png)

## docker 镜像(images)

Docker 把应用程序及其依赖，打包在 image 文件里面。只有通过这个文件，才能生成 Docker 容器。image 文件可以看作是容器的模板。Docker 根据 image 文件生成容器的实例。同一个 image 文件，可以生成多个同时运行的容器实例。(类似面向对象语言中类与实例的关系).

镜像构建时，会一层层叠加，前一层是后一层的基础.

![](https://img-blog.csdn.net/20170221093655867?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvMjFjbmJhbw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)




## docker 容器(containers)

## docker 仓库

## docker registy






