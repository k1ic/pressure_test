微观 (可用性)<br>
    cpu<br>
        衡量指标<br>
            平均延迟<br>
                测试工具：Cyclictest （https://cloud.tencent.com/developer/article/1053954）<br>
            使用率<br>
                观察工具：vmstat us sy id<br>
            运行队列<br>
                观察工具：vmstat r<br>
            上下文切换<br>
                观察工具：vmstat cs<br>
            综合<br>
                观察工具：top -c 1<br>
    内存<br>
        衡量指标<br>
            可用内存<br>
                观察工具：vmstat free<br>
            swap占用<br>
                观察工具：vmstat swpd<br>
            页面交换<br>
                观察工具：vmstat si so<br>
            内存坏位<br>
                测试工具：memtester（http://pyropus.ca/software/memtester/）<br>
                    测试目标：捕获内存错误、检测内存坏位<br>
                    测试项目：随机值、异或比较、减法、乘法、除法、与或运算<br>
    磁盘（以云盘为例）<br>
        衡量指标<br>
            使用率：<br>
                观察工具：iostat -dxk 1<br>
            IOPS：每秒读写(I/O)操作的次数，数值越高越好<br>
                测试工具：<br>
                    dd<br>
                    fio<br>
                    iozone（http://www.iozone.org/）<br>
            Throughput：每秒传输的MB字节数，一般用MBPS<br>
                测试工具：Orion （https://www.oracle.com/technetwork/cn/topics/index-088165-zhs.html）<br>
            Latency：完成一个 I/O 请求所需的时间<br>
                测试工具：ioping<br>
    网络<br>
        衡量指标<br>
            吞吐量：<br>
                测试工具：<br>
                    iftop -i eth0 -nNP<br>
宏观（稳定性）<br>
    unixbench<br>
        特点：经典linux跑分软件，便于对不同厂商相同配置服务器性能比较<br>
        项目地址：https://github.com/kdlucas/byte-unixbench<br>
        实测案例：https://github.com/bingjin/CloudTesting/tree/master/test_vm<br>
<br>
    ltp<br>
        特点：可为系统提供足够压力，常用于os超长时间压测<br>
        项目地址：https://github.com/linux-test-project/ltp<br>
        实测案例：https://www.ibm.com/developerworks/cn/linux/l-rel/index.html<br>
<br>
    sysbench<br>
        特点：多线程性能测试工具，可以测试CPU、内存、磁盘I/O、线程及数据库性能<br>
        项目地址：https://github.com/akopytov/sysbench<br>
        实测案例：http://www.cnblogs.com/zhoujinyi/archive/2013/04/19/3029134.html<br>
<br>
