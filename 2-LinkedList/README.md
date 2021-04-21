# LinkedList learning

1. [No.203 Remove Linked List Elements](https://github.com/Taki-L/Leet-Note/blob/main/2-LinkedList/203.md)
2. [No.707 Design Linked List](https://github.com/Taki-L/Leet-Note/blob/main/2-LinkedList/707.md)
3. [No.206 Reverse Linked List](https://github.com/Taki-L/Leet-Note/blob/main/2-LinkedList/206.md)

# 链表

单链表：

链表中的每个元素都是一个单独的对象，而所有对象都通过每个元素中的引用字段链接在一起

![image/Untitled%203.png](image/Untitled%203.png)

双链表：

与单链表不同的是，双链表的每个节点都含有两个引用字段

![image/Untitled%204.png](image/Untitled%204.png)

优点：

1. 能在O(1)时间内删除或者添加元素（单/双链表需要前/前后链表的信息）
2. 可以灵活的分配内存空间

缺点：

查询元素需要O(n)的时间

## 双链表示例

```cpp
//双向链表定义
typedef structdlink_node
{
	struct dlink_node *prev;
	struct dlink_node *next;
	void *val;
}node;
```

```cpp
//链表删除节点pindex
pindex -> next -> prev = pindex -> prev;
pindex -> prev -> next = pindex -> next;
free(pindex);  //删除后需要释放节点
```

```cpp
//将pnode节点插入到pindex之前
pnode -> prev = pindex -> prev;
pnode -> next = pindex;
pindex -> prev -> next = pnode;
pindex -> prev = pnode;
```

## 解题技巧

1. 利用快慢指针（有时需要三个指针）
2. 构建一个虚假链表头

    适用问题：

    1. 两个排序链表，进行整合排序
    2. 将链表的奇偶数按原定顺序分离，生成前半部分为奇数，后半部分为偶数的链表

    如果不用虚假链表头，在创建新链表第一个元素的时候，都需要判断一下链表头指针是否为空

## 训练技巧

- 在纸上或者白板上画出节点之间的相互关系
- 画出修改的方法

## 练习题：25. K个一组翻转链表

注：K=2时为24题

![image/Untitled%205.png](image/Untitled%205.png)
