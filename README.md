# 小样本图像分类的论文的学术地图记录
[目标榜单-SOTA]https://few-shot.yyliu.net

[PaperWithCode]https://paperswithcode.com/task/few-shot-image-classification
### 日常工作记录
- [x] 完成ATTENTIONAL CONSTELLATION NETS 的论文阅读+[调通代码](https://github.com/TJUdyk/ConstellationNet)
- [ ] 完成ReNEt的代码详细阅读 -打印出来Cross的图片
- [ ] 找到CrossAttentionNetwork的代码阅读和使用   
- [ ] 读代码：Constellation的代码阅读-Spatial attention和channelAttention
- [ ] 读CBAM和BAM看Spatial、attention、channel、和Branach的Attention如何结合
- [ ] 统一Spatial、Channel、Tempory、Branch的Attention机制，提出通用的注意力机制框架
- [ ] 实验的结果的可视化的操作和Cross-attention的代码（微信）
- [ ] 读SSformer的论文(已完成)看support和quey如何做patch的cross-attention
- [ ] 读No-Local的论文看Temporal的attention如何做的
- [ ] 读SeNet的论文和代码看channel attention如何做的，获得global context feature
- [ ] 读ConvMix的代码和论文（已完成），使用channel attention
- [ ] 参考论文vision permutator和S2MLPv2找到Branach attention相关的

### 读论文的顺序
- [x] Constellation Nets for Few-Shot Learning   ICLR 2021  
- [x] CrossViT- Cross-Attention Multi-Scale Vision Transformer for Image Classification 
- [x] A Universal Representation Transformer Layer for Few-Shot Image Classification
- [x] Cross Attention Network for Few-shot Classification
- [ ] ConTNet- Why not use convolution and transformer at the same time
- [x] Bottleneck Transformers for Visual Recognition
### Transformer相关论文
- [ ] A Survey of Visual Transformers
- [ ] Attention Mechanisms in Computer Vision（Attention综述读一下）
- [x] Bottleneck Transformers for Visual Recognition
- [x] Sparse Spatial Transformers for Few-Shot Learning
- [x] A Universal Representation Transformer Layer for Few-Shot Image Classification
- [ ] Escaping the Big Data Paradigm with Transformer
- [x] CrossViT- Cross-Attention Multi-Scale Vision Transformer for Image Classification 
- [x] Cross Attention Network for Few-shot Classification
- [x] Bottleneck Transformers for Visual Recognition
- [x] Few-shot Classification via Adaptive Attention
- [x] Constellation Nets for Few-Shot Learning   ICLR 2021  
- [ ] Dynamic Few-Shot Visual Learning without Forgetting  CVPR2018（记忆网络）
- [ ] ARE WE READY FOR A NEW PARADIGM SHIFT
- [x] RETHINKING ATTENTION WITH PERFORMERS 
- [x] Attention Mechanisms in Computer Vision
- [ ] ConTNet- Why not use convolution and transformer at the same time
- [ ] TRANSFORMERS FOR IMAGE RECOGNITION AT SCALE
- [ ] 论文vision permutator和S2MLPv2 （branach的attention）
- [ ] attention is not all you need 和patch are not all you need
- [ ] patch are all you need 中的CNN和Transformer结合的论文
- [ ] 读论文 protonet
### 注意力机制的论文 
- 最新的计算机视觉注意力机制(Attention)综述！[知乎Link](https://zhuanlan.zhihu.com/p/438524916)
- Patches are all you need?[知乎Link](https://www.zhihu.com/question/492712118/answer/2173720753)[PaperWithCode](https://paperswithcode.com/paper/patches-are-all-you-need)
- NeurIPS2021 港大&腾讯AI Lab&牛津提出：CARE，让CNN和Transformer能在对比学习中“互帮互助”！[CSDN Link](https://blog.csdn.net/moxibingdao/article/details/121219821)
- [ ] Are we ready for a new paradigm shift? A Survey on Visual Deep MLP [还在纠结CNN还是Transformer？清华发表一篇survey：全连接层才是终极答案！](https://zhuanlan.zhihu.com/p/437157898)
- [ ] 清华提出：最新的计算机视觉注意力机制综述(Attention)https://zhuanlan.zhihu.com/p/438524916
- [ ] 注意力机制（Visual Attention）https://zhuanlan.zhihu.com/p/324245989
- [ ] 注意力机制的Spatial Domain和Channel Domain https://blog.csdn.net/weixin_39552472/article/details/110746151

### 对自己提出一些问题-》多问几个为什么？
- Global Avg Pooling的作用GAP+FC的组合
- branach Attention 分别沿着HWC的三个channel做branch attention  参考论文vision permutator和S2MLPv2
### :heavy_check_mark: 关键的知识点
- 1*1卷积：好处是可以允许不同的channel和Spatial locations交流；坏处：让patch不再互相联系和receptive field消失
- 3*3卷积：receptive field受限制于neighbourhood来获得local representation，更大的receptive field对visual understanding很重要
- self-attention 可以看做可分离卷积（SpeConv）SCR和CCA模块都是用可分离卷积
- SCR模块使用1*1的卷积，但CCA模块不能使用
- vision Transformer make the pardigam shift to the area of global receptive field
- CNN的优点：inductive biases1：translation invariance和local connectivity
- 使用更大的卷积核来替代MLP和self-attention（可以mix distant Spatial locations）