## VIT(vision transformer)

ViT的介绍 ViT，全称为Vision Transformer，是一种基于Transformer架构的视觉处理模型。传统的计算机视觉任务通常使用卷积神经网络（CNN）来提取图像的特征。而ViT的目标是将Transformer模型应用于计算机视觉任务，通过全局性的注意力机制来捕捉图像中的长程依赖关系。

传统的Transformer模型在自然语言处理领域中取得了巨大的成功，但直接将其应用于图像处理任务面临一些挑战，因为图像数据的结构和特征与文本数据不同。ViT通过将图像数据划分为一系列的图像块（或称为图像补丁），并将这些图像块作为序列输入Transformer模型中，来处理图像数据。

ViT模型的基本组成包括：

输入编码：输入图像被划分为一系列的图像块，每个图像块经过线性映射（通常使用一个卷积层）后，被表示为一个向量序列。 Transformer编码器：ViT使用多个Transformer编码器层来处理输入的图像块序列。每个Transformer编码器层由自注意力机制（self-attention）和前馈神经网络（feed-forward network）组成。自注意力机制能够捕捉图像块之间的关联性，并对图像块进行上下文感知的特征表示。 分类头部：ViT模型的输出是通过一个额外的线性层进行分类预测。通常在最后一个Transformer编码器层的输出上应用全局平均池化操作，将图像块序列的特征聚合成一个全局特征向量，然后通过线性层进行分类。

ViT在一些图像分类、目标检测、语义分割等计算机视觉任务上表现出色，并在一些领域挑战中取得了竞赛水平的结果。它的优点之一是能够处理全局上下文信息，而不仅仅是局部特征，使其在处理大尺寸图像或具有长程依赖关系的任务上具有优势。然而，对于像素级细节或空间信息的精细处理，ViT可能需要更大的模型规模或其他辅助技术来提升性能。

[https://blog.csdn.net/wzk4869/article/details/130951275](https://blog.csdn.net/wzk4869/article/details/130951275)

## CLIP (Contrastive Language-Image Pretraining), Predict the most relevant text snippet given an image

CLIP的英文全称是**Contrastive Language-Image Pre-training**，即**一种基于对比文本-图像对的预训练方法或者模型**。CLIP是一种基于对比学习的多模态模型，与CV中的一些对比学习方法如moco和simclr不同的是，CLIP的训练数据是文本-图像对：一张图像和它对应的文本描述，这里希望通过对比学习，模型能够学习到文本-图像对的匹配关系。如下图所示，CLIP包括两个模型：**Text Encoder**和**Image Encoder**，其中Text Encoder用来提取文本的特征，可以采用NLP中常用的text transformer模型；而Image Encoder用来提取图像的特征，可以采用常用CNN模型或者vision transformer。

## Real-ESRGAN 高清放大算法[‣](https://github.com/xinntao/Real-ESRGAN)

[https://github.com/xinntao/Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)

将低分辨率图片/视频 高清化

## 图像分割算法 GroundingDINO 国人实现

[https://github.com/IDEA-Research/GroundingDINO](https://github.com/IDEA-Research/GroundingDINO)

知乎摘要

简单来说，Grounding DINO可以根据文字描述检测指定目标。例如下图左侧，你告诉它：“检测左边的狮子！”，它就会只把左边的狮子框选出来，是不是很神奇？当Grounding DINO和stable diffusion结合时，就会出现更加神奇的功能--自动P图。如下图右侧，你告诉它：“将左侧的狮子变成狗”，它就会帮你把左边的狮子P成狗。

### **背景介绍**

在视觉领域，要想达到真正的智能，那么对**新事物的理解**应该作为其一项基本能力。

在Grounding DINO中，作者想要完成这样一项任务：根据人类文字输入去检测任意类别的目标，称作**开放世界目标检测问题（open-set object detection）。**

![https://pic2.zhimg.com/80/v2-621f2f635aa740d25e2223a9daeca475_720w.webp](https://pic2.zhimg.com/80/v2-621f2f635aa740d25e2223a9daeca475_720w.webp)

[十分钟解读Grounding DINO-根据文字提示检测任意目标](https://zhuanlan.zhihu.com/p/627646794)

## SegmentAnything（SAM）

个人总结：对图像进行分割。

在SD中用于人物服装的更换,即识别出人物服装的部分，重绘实现换装。

[https://github.com/continue-revolution/sd-webui-segment-anything](https://github.com/continue-revolution/sd-webui-segment-anything)

## IPAdapter_plus

个人总的来说，该算法模型：将指定图的特征传递到生成图上；风格转换和艺术加工。

[https://github.com/cubiq/ComfyUI_IPAdapter_plus](https://github.com/cubiq/ComfyUI_IPAdapter_plus)

## InsightFace

著名的用于人脸识别的模型，由此诞生了InstantID