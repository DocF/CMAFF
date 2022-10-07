# Cross-Modality Attentive Feature Fusion for Object Detection in Multispectral Remote Sensing Imagery

Auhtor: FANG Qingyun and WANG Zhaokui


## Intro
#### CMAFF:Cross-Modality Attentive Feature Fusion 
<div align="left">
<img src="https://github.com/DocF/CMAFF/blob/main/yolofusion.png" width="700">
</div>

#### Differential Enhancive Module
<div align="left">
<img src="https://github.com/DocF/CMAFF/blob/main/DMEA.png" width="600">
</div>

#### Common Selective Module
<div align="left">
<img src="https://github.com/DocF/CMAFF/blob/main/CMSA.png" width="600">
</div>

Cross-modality fusing complementary information of multispectral remote sensing image pairs can improve the perception ability of detection algorithms, making them more robust and reliable for a wider range of applications, such as nighttime detection. Compared with prior methods, we think different features should be processed specifically, the modality-specific features should be retained and enhanced, while the modality-shared features should be cherry- picked from the RGB and thermal IR modalities. Following this idea, a novel and lightweight multispectral feature fusion approach with joint common-modality and differential-modality attentions are proposed, named Cross-Modality Attentive Feature Fusion (CMAFF). Given the intermediate feature maps of RGB and IR images, our module parallel infers attention maps from two separate modalities, common- and differential-modality, then the attention maps are multiplied to the input feature map respectively for adaptive feature enhancement or selection. Extensive experiments demonstrate that our proposed approach can achieve the state-of-the-art performance at a low computation cost.
For more details, please refer to [our paper](https://www.sciencedirect.com/science/article/abs/pii/S0031320322002679). 


## Citation
If you are interested this repo for your research, welcome to cite our paper:

```
@article{qingyun2022cross,
  title={Cross-Modality Attentive Feature Fusion for Object Detection in Multispectral Remote Sensing Imagery},
  author={Qingyun, Fang and Zhaokui, Wang},
  journal={Pattern Recognition},
  pages={108786},
  year={2022},
  publisher={Elsevier}
}
```



## Result
|Model|Attention|Params(M)|FLOPs(M)|MemR+W(MB)|
|:---------:|:---------:|:------------:|:-----:|:-----------------:|
|Yolov5l|MCFF_1|0.03|0.06|0.13|
||MCFF_2|0.06|0.13|0.26|
||MCFF_3|0.16|0.50|1.02|
||**Average**|0.08|0.23|0.47|
|Yolov5l|GFU_1|2.38|30400|103.25|
||GFU_2|9.50|30400|84.88|
||GFU_3|38.00|30400|175.44|
||**Average**|16.63|30400|121.19|
|Yolov5l|CMAFF_1|0.04|0.08|0.16|
||CMAFF_2|0.08|0.16|0.33|
||CMAFF_3|0.31|0.62|1.28|
||**Average**|0.14|0.29|0.59|
|Yolov5s|MCFF_1|0.02|0.03|0.07|
||MCFF_2|0.03|0.06|0.13|
||MCFF_3|0.06|0.13|0.26|
||**Average**|0.04|0.07|0.15|
|Yolov5s|GFU_1|0.59|7600|49.25|
||GFU_2|9.50|7600|32.94|
||GFU_3|38.00|7600|49.72|
||**Average**|4.16|7600|43.97|
|Yolov5s|CMAFF_1|0.02|0.04|0.08|
||CMAFF_2|0.04|0.08|0.16|
||CMAFF_3|0.08|0.16|0.33|
||**Average**|0.05|0.09|0.19|
