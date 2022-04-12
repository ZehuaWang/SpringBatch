SpringBatch 概述

Spring Batch是一个轻量级的 完善的批处理框架. 提供了大量可以重复使用的组件 包括日志, 追踪, 事务, 任务作业统计, 任务重启, 跳过, 重复, 资源管理. 对于大数据量和高性能的批处理任务, Spring Batch 同样提供了高级功能和特性来支持, 比如分区功能, 远程功能. 总之 Spring Batch可以支持简单的 复杂的和大数据量的批处理作业

Spring Batch是一个批处理应用框架, 不是调度框架. 但需要和调度框架合作来构建完成的批处理任务. 它只关注批处理任务相关的问题, 如事务, 并发, 监控, 执行等, 并不会提供相应的调度功能.

框架主要有以下的功能:

Transaction Management

Chucnk based processing

Declarative I/O

Start/Stop/Restart

Retry/Skip

![image](https://user-images.githubusercontent.com/40006814/163041955-21317f89-69e4-4266-ae1c-71cdfbf1a510.png)

框架一共有四个主要角色: Job Launcher是任务启动器, 通过它来启动任务, 可以看作是程序的入口. Job代表着一个具体的任务, Step代表一个具体的步骤

一个Job可以包含多个Step. JobRepository是存储数据的地方, 可以看作是一个数据库的接口. 在执行任务时需要通过它来记录任务状态的信息.
