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

## Acknowledgement
1. Annotations for this dataset are available at [the official repo of the challenge](https://github.com/wosdetc/challenge).
2. The heatmap generation using GradCAM (and etc.) are based on [YOLOv8 Explainer repo](https://github.com/Spritan/YOLOv8_Explainer).
3. The official ultralytics [repo](https://github.com/ultralytics/ultralytics).


## Cite this repository

Please cite our paper if this repo helps your research. The preprint will be released soon.

```
@InProceedings{Wong2025,
title = {WRN-YOLO: An Improved YOLO for Drone Detection using Wide ResNet},
author = {Yi Jie Wong and Wingates Voon and Mau-Luen Tham and Ban-Hoe Kwan and Yoong Choon Chang and Yan Chai Hum},
booktitle={2025 International Joint Conference on Neural Networks (IJCNN)},
year={2025}}
```
