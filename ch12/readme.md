## 优化问题
- 目标函数
- 约束条件集合
### 背包问题

|   | 攻击力  | 重量  | 价值/重量|
|---|---|---|---|
| item1  |  175  |  10  |  17.5 |
| item2  |  90  |  9  |  10 |
| item3  |  20  |  4  |  5 |
| item4  |  50  |  2  |  25 |
| item5  |  10  |  1  |  10 |
| item6  |  200  |  20  |  10 |

#### 选择价值最高物体
|   | 攻击力  | 重量  | 价值/重量|
|---|---|---|---|
| item6  |  200  |  20  |  10 |
一共可以得到 200 攻击力

#### 选择最轻的物件
|   | 攻击力  | 重量  | 价值/重量|
|---|---|---|---|
| item2  |  90  |  9  |  10 |
| item3  |  20  |  4  |  5 |
| item4  |  50  |  2  |  25 |
| item5  |  10  |  1  |  10 |
一共可以得到 170 攻击力

|   | 攻击力  | 重量  | 价值/重量|
|---|---|---|---|

问题是我们下面商品，weight 表示商品的重量 value 表示商品的价格，小偷的背包只能装 30 公斤的商品。那么问题是小偷怎么偷能够偷出更高的价格。

| weight  | value  |
|---|---|
| 2  | 3  |
| 3  | 4  |
| 4  | 5  |
| 5  | 8  |
| 9  | 10  |

#### 价格
B(k,w)
- k 表示前 k 个商品
- 表示剩余空间

我们假设偷到第 4 件商品，当第 5 件是否偷还是不偷，那么B(k,W) 中 W 是多少我们来计算一下
$$ w = 20 - (2 + 3 + 4 + 5) = 6$$
$$ B(k,w) \begin{cases}
    B(k - 1,w) \\
    max & \begin{cases}
        B(k-1,w - w_k) + v_k\\
        B(k-1,w)
    \end{cases} 
\end{cases}$$
| weight  | value  |
|---|---|
| 2  | 3  |
| 3  | 4  |
| 4  | 5  |
| 5  | 8  |

我们看看是否能够偷 k 

#### 0/1 背包问题的最优解
- 每一个item可用<攻击力,重量>来表示
- 游戏人物最多能够带 w 重量 item
- 用 n 维向量 I 表示 item 集合

#### 如何解决这个问题
- 枚举出有所物品的组合可能
- 从这些可能中去掉不满足条件组合(重量大于)
- 在满足条件组合中找到价值最大组合

### 图的最优化问题
#### 哥尼斯堡七桥问题
?描述复制即可

### 01 背包问题
有N件物品和一个容量是V的背包，在N件物品中第 i 件物品的体积是$v_i$ 价值是$w_i$
### 2 完全背包
### 多重背包问题
### 混合背包问题
### 二维费用的背包问题
### 分组背包问题
### 背包问题求方案数
### 背包问题方案
### 有依赖的背包问题


