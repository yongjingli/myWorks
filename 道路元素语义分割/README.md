# 基于深度学习的道路元素语义分割

首先在Full Convolution Network(FCN)的基础上，将Alexnet基网络替换为SE-ResNet50，以提高网络特征表达能力。将SE Attention模块改进为scSE Attention模块，在进行特征通道校准同时引入空间校准，以提升语义分割网络的细粒度。将下采样倍数由32改为16并精简网络，引入Atrous Spatial Pyramid Pooling(ASPP)模块，在提升网络分辨率的同时保证较大的感知野。在上采样部分引入Gated Feedback Refinement Network (G-FRNet)，利用Gating Mechanism将浅层特征和深层特征结合再通过Skip Connection传到Decode中，减少Encode浅层特征的歧义性。引入多路语义分割任务分支，有效解决分割元素多重属性问题，如车道线黄白和虚实属性。引入Weighted Loss减缓类别数据不平衡的问题，同时借助辅助Loss(不增加推理时间)，提升训练效果。 在常规数据增强方式的基础上，引入随机尺度等方法。最终，实现车道线，停止线和减速线等16类道路元素的分割提取，mIoU为0.81。

![image](https://github.com/yongjingli/myWorks/blob/master/%E9%81%93%E8%B7%AF%E5%85%83%E7%B4%A0%E8%AF%AD%E4%B9%89%E5%88%86%E5%89%B2/demo_sematic_segmetation.gif)
