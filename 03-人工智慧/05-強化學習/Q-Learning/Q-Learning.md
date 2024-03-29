# Q-Learning

Q-Learning 是一种强化学习算法，它的目的是帮助智能体学习如何通过执行不同的动作来最大化未来的奖励。

## 方程式

在 Q-Learning 中，我们使用一个称为 Q 表的数据结构来存储智能体在不同状态下执行不同动作的期望奖励。每次执行动作时，我们都会更新 Q 表，使用下面的公式：

$$Q(s, a) = (1 - \alpha) \cdot Q(s, a) + \alpha \cdot (R + \gamma \cdot \max_{a'} Q(s', a'))$$

其中，

$Q(s, a)$ 是节点 $s$ 使用动作 $a$ 后的期望得分
$\alpha$ 是一个动态调整的学习率参数
$R$ 是使用动作 $a$ 后获得的实际奖励
$\gamma$ 是一个衰减系数，用于权衡当前奖励和未来奖励的重要性
$s'$ 是使用动作 $a$ 后进入的新状态
$\max_{a'} Q(s', a')$ 表示在新状态 $s'$ 下执行的最佳动作的期望奖励
通过不断地更新 Q 表，智能体可以学习如何通过执行最佳动作来获得最大的期望奖励。


## 參考

* https://en.wikipedia.org/wiki/Q-learning
* [An Introduction to Q-Learning Part 2/2](https://huggingface.co/blog/deep-rl-q-part2)
