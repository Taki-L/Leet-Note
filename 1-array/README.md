# Array learning
Record the learning order of array questions

1. [No.35 Search Insert Position](https://github.com/Taki-L/Leet-Note/blob/main/1-array/35.md)
2. [No.27 Remove Element](https://github.com/Taki-L/Leet-Note/blob/main/1-array/27.md)
3. [No.209 Minimum Size Subarray Sum](https://github.com/Taki-L/Leet-Note/blob/main/1-array/209.md)
4. [No.59 Spiral Matrix II](https://github.com/Taki-L/Leet-Note/blob/main/1-array/59.md)

# Notes

优点：

1. 能在O(1)的时间里根据数组下标查询某个元素
2. 构建数组非常简单

缺点：

1. 构建时必须分配一段连续的空间
2. 查询某个元素是否存在是需要遍历整个数组，耗费O(n)的时间

![image/Untitled.png](image/Untitled.png)

Note：

- 数组是存放在连续空间上的相同类型数据的集合
- 正因为数组的内存空间地址是连续的，所以在删除或者增加元素的时候，就难免要移动其他元素的地址

![image/Untitled%201.png](image/Untitled%201.png)
