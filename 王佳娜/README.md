
# 个人信息
- 姓名：王佳娜
- 学号：21821112
- 主题：复杂网络（Complex Networks）
- 邮箱：cacyth@zju.edu.cn

# 论文选择

Determining the Diameter of Small World Networks

- Abstract：
In this paper we present a novel approach to determine the exact diameter (longest shortest path length) of large graphs, 
in particular of the nowadays frequently studied small world networks. Typical examples include social networks, 
gene networks, web graphs and internet topology networks. Due to complexity issues, the diameter is often calculated
based on a sample of only a fraction of the nodes in the graph, or some approximation algorithm is applied. 
We instead propose an exact algorithm that uses various lower and upper bounds as well as effective node selection 
and pruning strategies in order to evaluate only the critical nodes which ultimately determine the diameter. 
We will show that our algorithm is able to quickly determine the exact diameter of various large datasets of 
small world networks with millions of nodes and hundreds of millions of links, whereas before only approximations 
could be given.

- 摘要：
本文提出了一种确定大图，特别是目前研究较多的小世界网络的精确直径(最长路径长度)的新方法。 典型的例子包括社会网络，基因网络，网络图和互联网拓扑网络。 
由于复杂性问题，直径通常是基于图中一小部分节点的样本来计算的，或者应用一些近似演算法。 相反，我们提出了一个精确的算法，使用各种下界和上界，
以及有效的节点选择和剪枝策略，以评估的关键节点，最终确定的直径。 我们将展示我们的算法能够快速确定小世界网络中各种大型数据集的精确直径，
这些数据集包含数百万个节点和数亿个链接，而以前只能给出近似值。

- 引言：
图的直径被设计为图中任意两个节点之间的最长最短路径的长度。精确算法计算这个直径传统上需要运行一个所有对最短路径(APSP)算法为网络中的每个节点，最终返回的长度是最长的最短路径之一。虽然这将确实返回图的精确直径，复杂度是o(n3)为一般的加权图和o(mn)为稀疏的未加权图(有n个顶点和m条边)。这种计算直径的简单方法显然不适用于极大的图，例如有数百万个顶点和数十亿条边的图。
由于多种原因，直径是网络的一个相关性质。例如，在社交网络中，直径可以表示在最坏的情况下信息到达网络中每个人的速度。在一个科学协作网络中，一个高的直径可能表明有一些研究人员并没有非常紧密地合作。在因特网路由网络中，直径可以揭示网络中任意两台机器之间的最坏情况响应时间。
研究精确直径的一个优点是我们可以观察到实现直径的实际路径，这是一条我们在使用近似演算法或者仅仅通过观察网络样本来估计直径时得不到的信息。
本文的主要贡献是提出了一种确定小世界网络精确直径的新算法。在各种上下界和关键节点选择策略的基础上，对直线APSP算法进行了改进，并对现有的近似算法进行了改进，在几秒或几分钟内得到了具有数百万个节点的网络的精确直径。对小世界网络的各种大型数据集的性能进行了经验验证。

- 定义：
为了方便起见，我们提出了两个在本文中经常提到的与偏心率密切相关的组合问题。首先，单源最短路径问题是一个处理从单源顶点v2v到图中所有其他节点的所有最短路径的问题。对于非稀疏图，该问题具有传统的o(n2)时间复杂度(Dijkstra的最短路径算法)。当图是稀疏的，因此更容易存储使用邻接表，时间复杂性是有界的o(mlogn)。在我们的未加权的情况下，这甚至可以减少到o(m)，因为从起始节点到所有最短路径的广度优先搜索(BFS)都是确定的。本质上，为一个节点解决SSP问题意味着我们已经找到了该特定节点的偏心率。
其次，我们可以将全对最短路问题(APSP)定义为图的所有节点对之间的最短路问题，对于一般加权图，该问题的时间复杂度增加了一个因子n至o(n3)，对于稀疏的不加权图，增加了o(mn)。本质上，APSP算法获得的最大距离值是所有节点上的最大偏心距，因此等于图的直径。因此，如果我们解决APSP问题，我们已经找到了直径。

- 算法：
我们将从相邻节点的偏心性以及它们如何影响节点精度的观察开始。然后我们描述了我们的实际算法，称为边界直径，它利用这些观测值来改进APSP算法。接下来我们讨论了算法的复杂性和一些优化技术。
- 摘要：
- 摘要：
- 摘要：
