# 对象内存布局

## 对象头（Header）
* 第一部分（**Mark Word**）包括存储对象时的运行时数据：哈希码（HashCode）、GC分代年龄、锁状态标志、线程持有的锁、偏向线程ID、偏向时间戳等
* 第二部分是类型指针，指向类元数据的指针，数组对象还需记录数组的长度信息（对象访问定位-直接指针访问的情况）

## 实例数据（Instance Data）
* 存储对象在程序代码中所定义的各种类型的字段内容
* 存储顺序受虚拟机分配策略（FieldsAllocationStyle）和字段在Java源码中定义的顺序影响

## 对齐填充（Padding）
* 起到占位符的作用（Java中要求对象大小必须是8字节的整数倍）

[返回目录](../CONTENTS.md)