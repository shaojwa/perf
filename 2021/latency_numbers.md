偶然的机会了解到jeff dean提到的这一组数据，好像数据是09年的，现在网上一搜马上能看到2020年的版本。
具体什么版本关系不是很大，主要是对数据量级的理解。其实这组数据最开始是在peter norvig的个人主页上(http://norvig.com/21-days.html)

## 执行典型指令 1ns
这个很好理解，一条典型的指令一般在1ns以内，目前的CPU主频都是1-4GHz，考虑到一条典型的指令具体需要的周期并不是固定的。
所以，执行一条指令需要时间可以认为是ns量级。更为专业的分析可以参考这里（https://www.agner.org/optimize/instruction_tables.pdf）

## 从L1中获取数据
