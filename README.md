<div align="center">   
  
# MAESTRO: Task-Relevant Optimization via Adaptive Feature Enhancement and Suppression for Multi-task 3D Perception
</div>


> **MAESTRO: Task-Relevant Optimization via Adaptive Feature Enhancement and Suppression for Multi-task 3D Perception**, ICCV 2025.

> [Changwon Kang*], [Jison Kim*], [Hongjae Shin*], [Junseo Park], [Jun Won Choi]

>  [[PDF]](https://arxiv.org/pdf/2509.17462) [[Project]](https://rkdckddnjs9.github.io/)


## News
- [2023/09]: Our paper is on [arxiv](https://arxiv.org/pdf/2509.17462).
- [2025/07]: MAESTRO is accepted at ICCV 2025. 🔥
</br>


## Abstract
The goal of multi-task learning is to learn to conduct multiple tasks simultaneously based on a shared data representation. While this approach can improve learning efficiency, it may also cause performance degradation due to task conflicts that arise when optimizing the model for different objectives.
To address this challenge, we introduce MAESTRO, a structured framework designed to generate task-specific features and mitigate feature interference in multi-task 3D perception, including 3D object detection, bird's-eye view (BEV) map segmentation, and 3D occupancy prediction.
MAESTRO comprises three components: the Class-wise Prototype Generator (CPG), the Task-Specific Feature Generator (TSFG), and the Scene Prototype Aggregator (SPA).
CPG groups class categories into foreground and background groups and generates group-wise prototypes. The foreground and background prototypes are assigned to the 3D object detection task and the map segmentation task, respectively, while both are assigned to the 3D occupancy prediction task. TSFG leverages these prototype groups to retain task-relevant features while suppressing irrelevant features, thereby enhancing the performance for each task. SPA enhances the prototype groups assigned for 3D occupancy prediction by utilizing the information produced by the 3D object detection head and the map segmentation head. Extensive experiments on the nuScenes and Occ3D benchmarks demonstrate that MAESTRO consistently outperforms existing methods across 3D object detection, BEV map segmentation, and 3D occupancy prediction tasks.


## Method

| ![space-1.jpg](github_images/Overall_Architecture_v2.png) | 
|:--:| 
| ***Figure 1. Overall architecture of MAESTRO.** Multi-view images are processed by a shared backbone to generate a structured 3D voxel representation. The CPG generates foreground and background prototype groups, which guide the TSFG in refining task-relevant features for 3D object detection, BEV map segmentation, and 3D occupancy prediction. Task-oriented prototypes derived from the 3D object detection and BEV map segmentation heads are then integrated with the prototype groups via the SPA, forming Scene Prototypes. These Scene prototypes are subsequently processed by the occupancy decoder to produce the final 3D occupancy predictions.* |

## Getting Started
- [Installation](docs/install.md) 
- [Run and Eval](docs/getting_started.md)


## Dataset

- [x] nuScenes and Occ3D-nuScenes
- [ ] Waymo and Occ3D-Waymo

## Bibtex
If this work is useful for your research, please cite the following BibTeX entry.

```
@article{kang2025maestro,
  title={MAESTRO: Task-Relevant Optimization via Adaptive Feature Enhancement and Suppression for Multi-task 3D Perception},
  author={Kang, Changwon and Kim, Jisong and Shin, Hongjae and Park, Junseo and Choi, Jun Won},
  journal={arXiv preprint arXiv:2509.17462},
  year={2025}
}
```

## Acknowledgement

Many thanks to sophisticated open source projects:
- [mmdet3d](https://github.com/open-mmlab/mmdetection3d)
- [FlashOCC](https://github.com/Yzichen/FlashOCC)
- [OccFormer](https://github.com/Yzichen/FlashOCC)
- [BEVFusion](https://github.com/mit-han-lab/bevfusion)
- [CenterPoint](https://github.com/tianweiy/CenterPoint)
- [Occ3D](https://github.com/Tsinghua-MARS-Lab/Occ3D)
- [BEVDet](https://github.com/HuangJunJie2017/BEVDet)
- [ProtoOcc](https://github.com/SPA-junghokim/ProtoOcc)
