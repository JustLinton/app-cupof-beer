+++
date = "2011-05-15T21:57:17-07:00"
title = "DJ-Agent"
image = "dj-agent.png"
alt = "Osprey - minimalist blog and portfolio Hugo theme"
color = "#adacb0"
link1 = ""
link2 = ""

+++

By Jiuming Jiang | Key Words: Deep Reinforcement Learning, Music Generation, Python

![68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/68747470733a2f2f73312e617831782e636f6d2f323032322f30332f32322f714b647a38412e706e67.png)

### Publishing

First Author / Accepted by CISAI 2022 / Indexed by EI and Scopus

### What We Did

本文提出了一种结合音频分析和符号音乐生成的歌曲伴奏生成方法，从而可以利用人类音乐理论来构建强化学习模型，训练代理来创作音乐。

该算法的关键是从音频中提取音乐理论概念和一个在强化学习中效果很好的奖励模型。 然而，一些乐理规则很复杂，难以描述。 仅通过硬编码奖励很难获得有竞争力的结果。

This paper proposes a song accompaniment generation method that combines audio analysis and symbolic music generation so that human music theory can be used to build a reinforcement learning model, training an agent to create music. 

The key to this algorithm is to extract music theory concepts from audio and a reward model that works well in reinforcement learning. However, some music theory rules are complex and challenging to describe. It is difficult to achieve competitive results only by hardcoding the reward. 

![image-20220919112622003](https://linton-pics.oss-cn-beijing.aliyuncs.com/uPic/image-20220919112622003.png)

因此，为了建立一个有效的奖励模型，使用神经网络来评估作曲质量的感知部分，并使用程序辨别来对易于描述的音乐理论进行建模，两者协同工作。

实验表明，所提出的算法可以生成接近人类作曲家的伴奏安排，兼容各种音乐风格，并且在多个评估指标上优于基线算法。

Therefore, to build an effective reward model, a neural network is used to evaluate the perceptual part of composition quality, and program discrimination is used to model easy-to-describe music theory, and the two work together. 

Experiments show that the proposed algorithm can generate accompaniment arrangements close to human composers, is compatible with various musical styles, and outperforms the baseline algorithm in multiple evaluation metrics.

### Read More

| Click the links below to read more about the project.        |
| ------------------------------------------------------------ |
| [[Project Homepage]](https://github.com/JustLinton/dj-agent) |

