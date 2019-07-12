# nlp_tools
记录自己平时学习nlp过程中的工具和项目:laughing:    

如果github 上jupyter_notebook 打不开 可使用[nbviewer](https://nbviewer.jupyter.org/)打开，将网站复制进输入框即可
##  处理文本:books:

### 词向量
  1.若要使用预训练的词向量，不能简单的使用转化为小写，词干提取，删除非字母符等  
  2.要使预训练的词向量尽可能的覆盖到训练的文本，提高转化率   
    
  根据glove词向量预处理文本[link](https://github.com/XiaoQQin/nlp_tools/blob/master/process_text/process_pretrained_word2vec.ipynb)  
  参考链接[link](https://www.kaggle.com/christofhenkel/how-to-preprocessing-for-glove-part1-eda)
### 使用pack_padded_sequence 和 pad_packed_sequence
  在使用pytorch时，如果要采用双向的lstm，则要使用pack_padded_sequence 和 pad_packed_sequence。  
  [pack_padded_sequence](https://pytorch.org/docs/stable/nn.html#pack-padded-sequence)
  传入的两个参数 input 和lengths 分别为按照长度排好序的序列,lengths 为每个序列对应的长度  
  [pad_packed_sequence](https://pytorch.org/docs/stable/nn.html#pad-packed-sequence) 则在LSTM 后使用，直接使用即可  
  
  [pack_pad](https://github.com/XiaoQQin/nlp_tools/blob/master/pack_pad/pad.ipynb) 为一个函数，对输入的二维数据根据最长的序列长度进行pad，排序，返回初始序列的序号
