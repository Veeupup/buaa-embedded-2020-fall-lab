# sort.s 代码分析

过程参数分析

调用 sort
```
r0 buffer       数组指针
r1 bufferLen    数组长度
```

进入 sort
r3 i 初始化为 0

跳转到 .L2



