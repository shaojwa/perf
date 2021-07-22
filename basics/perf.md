#### 先看性能工具相关的脚本或者配置

如果是vdbench等工具性能问题，先看配置文件，关注open_flag，xfersize，fwdrate，iorate等大小。

对vdbench来说，默认的xfersize是4k，有时候可能不够。

对文件系统负载来说，尽管很多时候都是读写，这些是io操作，但有时候也有open，create，delete，mkdir等元数据操作，这些一般在vdbench中不认为是io 操作。

#### 看cpu数量和负载

uptime显示的负载如果大于nproc的数量2倍，一般就是比较繁忙，但是负载高并不代表cpu繁忙。

#### 确认是CPU密集还是IO密集

mptstat -P ALL 可以看到所有cpu的负载，如果idle达到都80%左右，也就是说一般cpu都不忙，此时留意一下iowait，如果这个比较高，说明io压力比较大。

#### 如果单个CPU较高，考虑是否有CPU亲和性问题
