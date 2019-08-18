
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->



<!-- /code_chunk_output -->

Linux中time命令，我们经常用来计算某个程序的运行耗时，用户态cpu耗时，系统态cpu耗时。

例如：

```
$ time foo 
real        0m0.003s
user        0m0.000s
sys         0m0.004s$
```

那么这三个时间都具体代表什么意思呢？

\[1] real : 表示foo程序整个的运行耗时，可以理解为foo运行开始时刻你看了一下手表，foo运行结束时，你又看了一下手表，两次时间的差值就是本次real 代表的值

举个极端的例子如下：可以看到real time恰好为2秒。

```
# time sleep 2

real    0m2.003s
user    0m0.000s
sys     0m0.000s
```

\[2] user   0m0.000s：这个时间代表的是foo运行在用户态的cpu时间，什么意思？

