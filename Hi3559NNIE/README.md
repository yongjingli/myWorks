# 海思移动平台部署嵌入式深度模型

负责在海思Hi3559的Neural Network Inference Engine(NNIE)平台部署嵌入式深度模型，包括分类，检测，分割，关键点检测和OCR等模型的量化转换和网络解析。完成AlexNet，GoogLeNet系列，ResNet和SqueezeNet等常用分类模型的转换和部署。实现Anchor-free的目标检测方法，提出Loss Pyramid Network(LPN)结构辅助神经网络的训练(不增加推理时间)，并结合上下文信息进一步提高了网络的识别精度，在30万像素的输入下该神经网络的运算速度达到30fps。语义分割和检测网络采用两路NNIE的形式同时运算，语义分割Argmax后处理部分采用图像分块多线程并行运行方式以提高后处理速度 在30万像素的输入下，该神经网络的运算速度达到20fps。实现Realtime Multi Person Pose Estimation人体关键点检测模型转换和部署，主要完成Heatmap分支的解析。实现基于CNN+LSTM+CTC的车牌识别模型训练、转换和部署，在CCPD数据集合的准确率达到99%。

# Anchor Free Detection
![image](https://github.com/yongjingli/myWorks/blob/master/videos/demo_person_car.gif)

# 基于人体关键点的手势识别
![image](https://github.com/yongjingli/myWorks/blob/master/videos/demo_gs.gif)

# CNN+LSTM+CTC的车牌识别
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_1-%E7%B2%A4.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_1-%E7%9A%96AF105N-0_33_38_58_57_62_45.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_9-%E7%90%BCFQ6MZD-21_38_47_63_44_56_36.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_9-%E8%B4%B5LXYTH6-23_43_54_55_50_40_63.jpg)

![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_1-%E6%B5%99BM0T03-11_34_44_57_50_57_60.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_1-%E7%9A%96A0U333-0_33_57_51_60_60_60.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_9-%E9%B2%81TXJ2Q1-15_50_54_41_59_47_58.jpg)
![image](https://github.com/yongjingli/myWorks/blob/master/images/resultID_9-%E7%B2%A4RCNTHH-19_48_35_45_50_40_40.jpg)
