程序的核心是用一个结构体 map 的双向链表来显示模拟内存的释放与存储情况
使用fmalloc(100) 用来申请分配100的内存空间
使用free(100, addr) 用来释放addr后面100空间的内存
在匹配多个零散分布的内存区间(结构体map记录模拟)时采用首次适应法
在第一次找到匹配的内存块的时候就进行分配
在使用ffree进行释放内存时不考虑跨越多个内存块区间进行合并清空
只针对单个占用的内存区间进行了课本上4种情况下的释放以及对结构体map的更新

