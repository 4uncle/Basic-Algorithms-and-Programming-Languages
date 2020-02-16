# 基本编程语言入门以及常用算法
## python
> [python入门](https://github.com/4uncle/Basic-Algorithms-and-Programming-Languages/blob/master/python/Python入门学习.md)




### 199 . 二叉树右视图

**题目描述**

> 给定一棵二叉树，想象自己站在它的右侧，按照从顶部到底部的顺序，返回从右侧所能看到的节点值。
>
> ```js
> 输入: [1,2,3,null,5,null,4]
> 输出: [1, 3, 4]
> 解释:
> 
> 1            <---
> /   \
> 2     3         <---
> \     \
> 5     4       <---
> 
> 来源：力扣（LeetCode）
> 链接：https://leetcode-cn.com/problems/binary-tree-right-side-view
> 著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。
> ```

**解答**

![](https://user-gold-cdn.xitu.io/2020/2/17/1704ee16cbb2891a?w=480&h=463&f=png&s=79526)

![](https://user-gold-cdn.xitu.io/2020/2/17/1704ee2cb31307c9?w=480&h=333&f=png&s=88204)

> **按照层次遍历，写入双端队列，从队列弹出数据根据层次筛选写入hashMap**
>
> ```python
> @param depth :层数
> @param node : 节点
> map[0]=1
> map[1]=2, map[1]=3
> map[2]=4,map[2]=5,map[2]=6
> ...
> map[depth]=node.val
> 
> loop: index: 0 ~ depth
>   result.append(map[index])
>   
> result = [1,3,6.....]
> ```
>
> 

**代码**

> ```python
> from collections import deque
> 
> 
> class TreeNode:
>     def __init__(self, x):
>         self.val = x
>         self.left = None
>         self.right = None
> 
> 
> class Solution(object):
> 
>     def rightSideView(self, root):
>         # 记录层次遍历的最右端数据
>         rigth_most_value_at_depth = dict()
>         # 最大深度
>         max_depth = -1
>         # 初始化双端队列
>         queue = deque([(root, 0)])
>         while queue:
>             # 左端出队
>             node, depth = queue.popleft()
>             # 若节点不为空
>             if node is not None:
>                 # 增加最大深度
>                 max_depth = max(max_depth, depth)
>                 # 结果集赋值
>                 rigth_most_value_at_depth[depth] = node.val
>                 # 将左右子树从右端树压入队列
>                 queue.append((node.left, depth + 1))
>                 queue.append((node.right, depth + 1))
>         return [rigth_most_value_at_depth[depth] for depth in range(max_depth + 1)]
> ```
>
> 

