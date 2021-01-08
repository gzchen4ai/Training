# ICPC2020-上海站（VP）

$Author:Rayment$

## 总结

开场看I题，觉得可做，发现一个点到另一个点的最短路线应该只会有三种决策，不妨假设从大圆弧上出发，到小圆弧上结束，那么第一种是下到小圆弧上再绕过去，第二种是直接冲圆心走，第三种是下到某个更小的圆弧，从上面绕过去。当时在思考第三种情况是不是存在，不过没有继续深入去证明结论了。

然后去读了J题

## 解题报告

### I.Sky Garden

**题意**

给你 $n$ 个以原点为圆心，且半径分别为 $1,2,\cdots,n$ 的圆，以及 $m$ 条过原点的直线，且恰好把每个圆分成 $2m$ 个相等的圆弧。求这 $n+m$ 个图形构成的所有的交点，两两之间的最短距离的和，注意两点之间的最短距离只计算一遍。

$1\leq n,m\leq 500$

**题解**

发现一个点到另一个点的最短路线应该只会有三种决策，不妨假设从大圆弧上出发，到小圆弧上结束，那么第一种是下到小圆弧上再绕过去，第二种是下到某个更小的圆弧$0\leq r$，从上面绕过去。

比较两种决策。假设三条圆弧 $r < i \leq j$ ，且跨过的弧度之差为 $\theta$ ，若第三种决策优于第一种决策，那么 $(j-i)+2(i-r)+r\theta < (j-i) + i \theta$，化简得到 $r(\theta -2) < i(\theta -2)$，不难发现当 $\theta > 2$ 时，选择 $r=0$ 的圆弧最优，否则选择第一种决策

那么枚举大圆弧和小圆弧的半径，再枚举两个点之间相差的弧度即可做到 $O(n^2m)$。需要注意的是当 $m>1$ 时，原点才是一个交点。

### J.Octasection

**题意**



### K.Traveling Merchant

