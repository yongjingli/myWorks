# 基于深度学习的道路设施目标检测

负责实现高精度地图下的交通标志和交通灯目标检测任务。为解决小目标（如交通灯）和难区分目标（如限速和限高）的检测识别问题，采用Yolov3目标检测+SE-ResNet50分类器的策略：首先采用Yolov3对交通灯，提示，警告和禁止交通标志进行目标检测，然后利用SE-ResNet50对交通标志检测结果进行进一步的分类，如区分不同的限速，限高等。该策略对于提升识别效果，进行样本标注和添加新类都有较大的好处。采用的目标检测框架为Yolov3，其在具有速度优势的前提下，具有不错的预测精度和小物体的识别能力。Yolov3的Backbone为Darknet53，通过引入Feature Pyramid Network（FPN）、多尺度预测和Anchors机制等方式以提高小目标的识别效果和召回率。采用多尺度输入、Sub-batchsize和Burn-in等方式来降低显存的要求和充分优化网络。基于该框架，实现交通灯，提示，警告和禁止交通标志目标检，测评的mAP为0.827，并进一步将该框架作为Third-Src，封装接口和编写Cmaklist，用于实际工程。

![image](https://github.com/yongjingli/myWorks/blob/master/videos/demo_yolov3.gif)

