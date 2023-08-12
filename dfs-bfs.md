# algorithm-learning
个人学习记录  Personal learning record

## dfs、bfs

### 染色法
例题：[拯救oibh总部](https://www.luogu.com.cn/problem/P1506)  
题解：[简单易懂](https://www.luogu.com.cn/blog/mengxindeboke/solution-p1506)

例题：[海战](https://www.luogu.com.cn/problem/P1331)   
笔记：   
需要考虑位置不正确的情况，可以直接暴力遍历一遍是否存在不正确的地方，然后再bfs。   
关键是想到位置不正确是什么样的情况。  
>这道题的难点在于判断是否有船相邻。
>通过自己模拟的数据可以得出结论： 
>如果图是不和法的，一定存在如下结构：  
>\# #   
>. #  
>或  
>\# #  
>\# .  
>或  
>\# .  
>\# #  
>或  
>. #  
>\# #  
>即在一个2*2的方格中有三个#

例题；[01迷宫](https://www.luogu.com.cn/problem/P1141)   
笔记：
这道题bfs和dfs都可以用，关键是如何减少时间复杂度，否则就会有几个点一直TEL。
优化的关键是要注意到   
>对于任意两个点A,B，如果a能遍历到b那么b一定能遍历到a，b能遍历到的点数一定与a相等  
所以可以使用连通块或者染色，把在同一连通块的点染成同一颜色，然后在询问点的时候如果已经染了色就可以直接输出相对应的cnt 


