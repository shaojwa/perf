## 几个基本概念
* work load

## 参数
#### time_based
一直持续这么久，即使文件已经完成读写，也会重复执行。要是无法估计运行时长，那就不要设置该选项，比如预埋数据时。

#### thread
感觉是并发模式，是线程模式，还是进程模式，用pthread_create创建线程，而不是fork来创建进程。

#### numjobs
任务数量，默认数量是1。从进程内的线程上看，fio，log，service，admin_socket等线程都翻倍。

#### iodepth
队列深度

#### direct
相当于打开文件时添加O_DIRECT选项，不适用缓冲。在linux下比较常用，支持比较好。

#### buffered
相对direct，使用缓存。

## 输出
|输出字段参数|含义|
|:-|:-|
|slat|submit latency，提交时延，从创建到提交，其中stdev表示标准差|
|clat|完成时延，从提交到完成，对于同步IO来说，政治几乎为0|
|lat|从IO创建到完成，整个事件|
