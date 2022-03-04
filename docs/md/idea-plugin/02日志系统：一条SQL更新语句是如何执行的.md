## 02 | 日志系统:一条SQL更新语句是如何执行的？

1. redo log(存储引擎 InnoDB特有 循环写 crash-safe(当数据库宕机时重启后数据不会丢失))

   InnoDB的redo log为固定大小， 它读写文件为磁盘顺序读写。

   write pos:当前位置。

   check point:当前要擦除的位置，擦除前要把记录更新到数据文件。

   write pos与check point之间为剩余空间，当不够时check point会向前推进。

   <img src="https://static001.geekbang.org/resource/image/16/a7/16a7950217b3f0f4ed02db5db59562a7.png" alt="img" style="zoom: 50%;" />

2. bin log(Server层 追加写 主要用于归档)

   bin log文件写满时不会清除之前的数据。

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   