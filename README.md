# Waterbro's Reading List on Natural Language Processing


### Character-level Convolutional Networks for Text Classification, NIPS, 2015
* 即char CNN。用CNN做文本分类，方法是对于每一个字母做一个one-hot的向量，然后拉长序列长度，大约70x1000作为CNN的输入。

### A large annotated corpus for learning natural language inference，ACL，2015
* 本文中提出了一个数据集，是当时最大的，构建方法是，先提供photo的标题作为premise（前序文本），让人来提出三个hypothesis（假设文本），分别是蕴含关系（即两个说的意思逻辑对的上），中立关系和矛盾关系（两句话不可能同时发生），然后有一个验证环节，就是再找人来判断每一组pair是什么关系。
* 这里面提到的分类方法，由词的向量构建句子向量怎么样更合理，虽然LSTM确实是最好的结果，但是直接把词向量求平均也差的不远。

### Efficient Estimation of Word Representations in Vector Space，ICLR，2013
* word2vec的第一篇文章，这里面的核心idea是如何让词与词之间有关系，什么样的次在embedding空间应该离得近？这篇文章的角度是同一句话中，上下文的词在空间中应该离得近。
* 做法是训练两个输出，一个输出的任务是用context词语预测center词语，另一个是用center词语预测context，都是分类任务。

### GloVe: Global Vectors for Word Representation，EMNLP，2014
* 用优化的方法解决word embedding在空间中语义上相近的空间中也近。通过对共生矩阵的一系列推导来得出优化目标。
* 优点是训练很快，而且和语料库的大小也无关。
* 常见的evaluate方法是计算比如a is to b like c is to ？看看word vector里面是不是a-b+c=d。

### Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation，EMNLP，2014
* 提出GRU，gated recurrent unit的文章，它的实现比lstm要简单。
* lstm和gru在大多数场景下性能是差不多的，在long term上也都比普通rnn要好。不过当问题变得复杂的时候lstm会好一点。


