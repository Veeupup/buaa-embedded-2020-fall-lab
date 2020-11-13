# sort.s 代码分析

直接看代码

栈中的值
r7,#4   buffer
r7      bufferLen
r7,#20  i
r7,#16  j

过程参数分析

调用 sort
```
r0 buffer       数组指针
r1 bufferLen    数组长度
r7 #sp          栈指针
buffer r0 保存到 [r7+4]
bufferLen r1 保存到 [r7]
r3 i 初始化为 0
i r3 保存到 [r7+20]
跳转到 .L2
```

.L2
```
取出 r2 = [r7+20](i)
取出 r3 = [r7] (bufferLen)
如果 i < bufferLen，那么跳转到 .L6
```

.L6
```
保存 r3 到 [r7+16] j
跳转到 .L3
```

.L3
```
没有 str 没有保存新的值
r3 = j
判断 j是否小于 bufferLen - i - 1

```

.L5
```
r3 = j


```
