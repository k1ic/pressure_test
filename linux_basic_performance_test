微观 (可用性)
    cpu
        衡量指标
            平均延迟
                测试工具：Cyclictest （https://cloud.tencent.com/developer/article/1053954）
            使用率
                观察工具：vmstat us sy id
            运行队列
                观察工具：vmstat r
            上下文切换
                观察工具：vmstat cs
            综合
                观察工具：top -c 1
    内存
        衡量指标
            可用内存
                观察工具：vmstat free
            swap占用
                观察工具：vmstat swpd
            页面交换
                观察工具：vmstat si so
            内存坏位
                测试工具：memtester（http://pyropus.ca/software/memtester/）
                    测试目标：捕获内存错误、检测内存坏位
                    测试项目：随机值、异或比较、减法、乘法、除法、与或运算
    磁盘（以云盘为例）
        衡量指标
            使用率：
                观察工具：iostat -dxk 1
            IOPS：每秒读写(I/O)操作的次数，数值越高越好
                测试工具：
                    dd
                    fio
                    iozone（http://www.iozone.org/）
            Throughput：每秒传输的MB字节数，一般用MBPS
                测试工具：Orion （https://www.oracle.com/technetwork/cn/topics/index-088165-zhs.html）
            Latency：完成一个 I/O 请求所需的时间
                测试工具：ioping
    网络
        衡量指标
            吞吐量：
                测试工具：
                    iftop -i eth0 -nNP
宏观（稳定性）
    unixbench
        特点：经典linux跑分软件，便于对不同厂商相同配置服务器性能比较
        项目地址：https://github.com/kdlucas/byte-unixbench
        实测案例：https://github.com/bingjin/CloudTesting/tree/master/test_vm

    ltp
        特点：可为系统提供足够压力，常用于os超长时间压测
        项目地址：https://github.com/linux-test-project/ltp
        实测案例：https://www.ibm.com/developerworks/cn/linux/l-rel/index.html

    sysbench
        特点：多线程性能测试工具，可以测试CPU、内存、磁盘I/O、线程及数据库性能
        项目地址：https://github.com/akopytov/sysbench
        实测案例：http://www.cnblogs.com/zhoujinyi/archive/2013/04/19/3029134.html
