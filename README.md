# WRN-YOLO: An Improved YOLO for Drone Detection using Wide ResNet

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1njhNZjqhaFlISCtd4R_yW_BGJGQt46EG?usp=sharing)

#### By [Yi Jie WONG](https://github.com/yjwong1999) et al

This code is our solution for the [8th WOSDETC Drone-vs-Bird Detection Challenge](https://wosdetc2025.wordpress.com/), hosted at IJCNN 2025. Specifically, this repository provides the code to create our proposed WRN-YOLO and the synthetic dataset used in our submission. Our approach ranked Top 3 globally in the challenge! 🏅🎉🥳

## Setup environment
```bash
pip install ultralytics==8.3.71
pip install grad-cam==1.5.4
```

## Dataset
The dataset was provided by the [WOSDETC](https://github.com/wosdetc/challenge) Drone-vs-Bird Detection Challenge [@IJCNN2025](https://2025.ijcnn.org/) committee. To aquire the dataset you may follow the instructions [here](https://wosdetc2025.wordpress.com/instruction-for-authors/). You will be asked to sign a data usage agreement and can then use the data for research purposes.  

Meanwhile, you can also download our synthetic dataset in [roboflow](https://universe.roboflow.com/project-psbzx/synthetic-fenky).


## Future Works
1. Consider using SAHI, and evaluate using [SAHI evaluation code](https://github.com/ultralytics/ultralytics/issues/7768#issuecomment-1906360471)
2. Add birds as distraction objects

   

## YOLO backbone & architecture customization

Ultralytics currently support customization of backbone using pretrained models from `TorchVision`. You can refer [my tutorial](https://github.com/yjwong1999/simpleCustomYOLO) to learn more about the customization. In this competition, I customize YOLOv5 backbone using `Wide-ResNet-2` backbone from `TorchVision`. 

Meanwhile, I have created an [ultralytics PR](https://github.com/ultralytics/ultralytics/pull/19609) which support backbone customization using `Timm`. Specifically, `Timm` has much more choices of pretrained backbones with different pretrained weights and etc. I am happy that this PR contributes to [17th out of ~1200 teams](https://github.com/ultralytics/ultralytics/pull/19609#issuecomment-2942623469) for one of my PR users 😄. Also, I used this `Timm` backbone customization in my another [ICIP competition](https://github.com/yjwong1999/Double_J_CADOT_Challenge). You can refer [my tutorial](https://github.com/ultralytics/ultralytics/pull/19609#issue-2906095221).

```bash
pip install git+https://github.com/DoubleY-BEGC2024/ultralytics-timm.git
```



## Cite this repository

If this repo or my tutorial on backbone customization helps your research, please kindly star this repo and cite our paper 😄 The preprint can be found [here](https://doi.org/10.36227/techrxiv.174495627.74350303/v1)!

```
@InProceedings{Wong2025,
title = {WRN-YOLO: An Improved YOLO for Drone Detection using Wide ResNet},
author = {Yi Jie Wong and Wingates Voon and Mau-Luen Tham and Ban-Hoe Kwan and Yoong Choon Chang and Yan Chai Hum},
booktitle={2025 International Joint Conference on Neural Networks (IJCNN)},
year={2025}}
```


## Acknowledgement
1. Annotations for this dataset are available at [the official repo of the challenge](https://github.com/wosdetc/challenge).
2. The heatmap generation using GradCAM (and etc.) are based on [YOLOv8 Explainer repo](https://github.com/Spritan/YOLOv8_Explainer).
3. The official ultralytics [repo](https://github.com/ultralytics/ultralytics).
