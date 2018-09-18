# Waterbro's Reading List on Natural Language Processing


### Character-level Convolutional Networks for Text Classification, NIPS, 2016
* 即char CNN。用CNN做文本分类，方法是对于每一个字母做一个one-hot的向量，然后拉长序列长度，大约70x1000作为CNN的输入。

### A large annotated corpus for learning natural language inference，ACL，2015
* 本文中提出了一个数据集，是当时最大的，构建方法是，先提供photo的标题作为premise（前序文本），让人来提出三个hypothesis（假设文本），分别是蕴含关系（即两个说的意思逻辑对的上），中立关系和矛盾关系（两句话不可能同时发生），然后有一个验证环节，就是再找人来判断每一组pair是什么关系。
* 这里面提到的分类方法，由词的向量构建句子向量怎么样更合理，虽然LSTM确实是最好的结果，但是直接把词向量求平均也差的不远。

