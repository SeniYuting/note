# 用Salt监控系统
## 监控基础
### 使用Salt读取系统核心信息
* 早期的Salt模块设计用来收集各种各样的配置信息，解析并按易用的格式进行格式化后返回给用户；多数系统核心相关的信息都在status模块

## 使用Returner监控系统
* Returner可以用外部数据存储器来存储从Minion任务返回的数据，对监控而言这是理想的状态信息，因为外部数据存储可以建立一条基线

## 使用监控State
* 每个独立的State都会返回4种信息：Name、Result、Changes和Comment，而监控State和标准State有3种不同：
```
1. 监控State不允许对系统进行修改，其任务只是监测和报告；
2. 监控State返回第5种信息：Data；
3. 当一个监控State被调用时，可以给出参数，定义哪些数据字段被认为是可接受的；
```

## 使用beacon
* beacon允许第三方进程触发事件，无须在进程自身中做太多处理
* beacon设计的目的是为了监控，尤其是告警

### 监控文件变化
* beacon会在目标Minion上定期运行

[返回目录](../CONTENTS.md)