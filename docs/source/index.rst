.. XuanPolicy documentation master file, created by
   sphinx-quickstart on Wed May 31 20:18:19 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

欢迎来到‘玄策’中文文档!
======================================

**XuanPolicy** is an open-source ensemble of Deep Reinforcement Learning (DRL) algorithm implementations.
**玄策** 是一个深度强化学习（Deep Reinforcement Learning, DRL）开源算法库。“玄”字意为玄妙的，“策”意为策略。
在深度强化学习算法中，智能体通过和环境交互不断试错，最终学习出一个最优策略完成任务，而不需要对环境或动力学模型建立精确的模型，因此该算法库被称为“玄妙的策略”，故而取名“玄策”。

此外，虽然深度强化学习能够解决很多复杂的任务，但是在算法调试的过程中，深度神经网络和优化过程对超参数往往比较敏感。
对于某特殊结构的算法，要想调出一组最佳的超参数，往往需要开发人员进行大量的试错。
由于对超参数调试的方法主要以来开发人员的经验，难以总结出一条通用的规律，因此常被戏称为“玄学”。
而该算法库提供了大量目前主流的DRL算法，其实现过程易于理解，使得算法的复现不再玄学。
“玄策”的适用人群包括但不限于：人工智能方向学生，DRL开发人员，DRL入门学习者，等。

“玄策”目前同时支持多种深度学习框架，包括
PyTorch_，
TensorFlow_，和
MindSpore_。并且支持CPU、GPU运算，能够在Linux，Windows，MacOS等操作系统上运行。

.. _PyTorch: https://pytorch.org/
.. _TensorFlow: https://www.tensorflow.org/
.. _MindSpore: https://www.mindspore.cn/en

.. toctree::
   :maxdepth: 1
   :caption: 如何使用:

   documents/usage/installation
   documents/usage/basic_usage
   documents/usage/professional_usage

.. toctree::
   :maxdepth: 1
   :caption: 主要模块与功能介绍:

   documents/structure/common
   documents/structure/environments
   documents/structure/representations
   documents/structure/policies
   documents/structure/agents
   documents/structure/learners

.. toctree::
   :maxdepth: 1
   :caption: API详细介绍:

   documents/api_tutorial/common

.. toctree::
   :maxdepth: 1
   :caption: 算法介绍:

   documents/agents/index_drl
   documents/agents/index_marl

.. toctree::
   :maxdepth: 1
   :caption: 参考基准

   documents/benchmark/toy
   documents/benchmark/mujoco
   documents/benchmark/atari
   documents/benchmark/mpe
   documents/benchmark/magent

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
