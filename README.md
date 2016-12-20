# jaylyrics_generation_tensorflow
使用基于LSTM的seq2seq模型并结合注意力机制来生成周杰伦歌词，详情请关注我的微信公众号：deeplearningdigest

## 环境
基于Tensorflow rc0.12版本，Python2.7，支持CPU/GPU。

## 训练
`python train.py `

如果要使用基于注意力的解码器，那么请在train.py文件中指定attention为True，或者在命令行使用如下：

`python train.py attention=True `

## 抽样生成单词
`python sample.py `

抽样有三种方法，分别是argmax、weighted、combined，它们的作用分别是

`argmax `:每一步都是根据分布概率得到概率最大的那个汉字

`weighted `:每一步都是根据概率分布抽样得到汉字

`combined `:每次遇到句号时，就会根据概率分布抽样；而其余情况都是得到概率最大的汉字

## 生成序列案例
使用`从前`作为种子序列，生成歌词如下：

```
从前进开封 出水芙蓉加了星
在狂风叫我的爱情 让你更暖
心上人在脑海别让人的感觉
想哭 是加了糖果
船舱小屋上的锈却现有没有在这感觉
你的美 没有在
我却很专心分化
还记得
原来我怕你不在 我不是别人
要怎么证明我没力气 我不用 三个马蹄
生命潦草我在蓝脸喜欢笑
中古世界的青春的我
而她被芒草割伤
我等月光落在黑蝴蝶
外婆她却很想多笑对你不懂 我走也绝不会比较多
反方向左右都逢源不恐 只能永远读着对白
```


