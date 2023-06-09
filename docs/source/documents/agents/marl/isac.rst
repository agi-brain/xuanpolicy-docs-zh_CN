ISAC
======================

算法描述
----------------------

ISAC算法全称为independent soft actor-critic based on maximum entropy，
是一种基于执行器-评价器（actor-critic based）的多智能体深度强化学习算法。
ISAC算法是一种独立训练和独立执行的多智能体强化学习算法，每个智能体的值函数输入空间只有自己的观测和动作，
同样智能体也只根据自身观测的数据进行决策。
ISAC分别使用不同的神经网络来拟合智能体的策略和值函数，其中拟合策略的神经网络输出的是高斯分布，
主要用于解决连续动作空间下的多智能体控制问题。ISAC算法中的每个智能体最大化自身的累计奖励和策略的熵。

在本算法库中，ISAC应用于三个智能体强化学习任务场景。
每个智能体的前向传播分为representation，eval_policy, eval_Q三个部分。
representation由包含单隐层的多层感知器MLP构成，输入为智能体观测的状态信息，输出为64维的隐状态信息。
eval_a 模块的输入为representation的输出，再次经过单隐层的MLP网络输出动作的高斯分布，
每个智能体通过在高斯分布中采样选择最后施加于环境中的动作。
Eval_Q模块的输入为representation的输出，再次经过单隐层的MLP网络值函数。
此外，ISAC中的每个智能体还包含target_a和target_Q作为目标动作网络和目标Q网络，
目标网络与在线网络结构系统相同，参数和在线网络保持周期性一致。
