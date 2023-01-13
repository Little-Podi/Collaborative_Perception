# Collaborative Perception

This repository is a paper digest of recent advances in **collaborative** / **cooperative** / **multi-agent** perception for **V2I** / **V2V** / **V2X** autonomous driving scenario. Papers are listed in alphabetical order of the first character.



## :star2:Recommendation

### Helpful Learning Resource:thumbsup::thumbsup::thumbsup:

- **(Talk)** Robust Collaborative Perception against Communication Interruption [[video](https://www.youtube.com/watch?v=3cIWpMrsyeE)], Collaborative and Adversarial 3D Perception for Autonomous Driving [[video](https://www.youtube.com/watch?v=W-AONQMfGi0)], Adversarial Robustness for Self-Driving [[video](https://www.youtube.com/watch?v=8uBFXzyII5Y)], Vehicle-to-Vehicle Communication for Self-Driving [[video](https://www.youtube.com/watch?v=oikdOpmIoc4)], 基于群体协作的超视距态势感知 [[video](https://www.koushare.com/video/videodetail/33015)], 协同自动驾驶：仿真与感知 [[video](https://course.zhidx.com/c/MmQ1YWUyMzM1M2I3YzVlZjE1NzM=)], 新一代协作感知Where2comm减少通信带宽十万倍 [[video](https://www.techbeat.net/talk-info?id=727)], 基于V2X的多源协同感知技术初探 [[video](https://www.bilibili.com/video/BV13v4y197Vc/)], 面向车路协同的群智机器网络 [[video](https://www.bilibili.com/video/BV1rV4y1w7kE/)]
- **(Survey)** Collaborative Perception for Autonomous Driving: Current Status and Future Trend [[paper](https://arxiv.org/abs/2208.10371)], A Survey and Framework of Cooperative Perception: From Heterogeneous Singleton to Hierarchical Cooperation [[paper](https://arxiv.org/abs/2208.10590)]
- **(Library)** CoPerception: SDK for Collaborative Perception [[code](https://github.com/coperception/coperception)] [[doc](https://coperception.readthedocs.io/en/latest/)], OpenCOOD: Open Cooperative Detection Framework for Autonomous Driving [[code](https://github.com/DerrickXuNu/OpenCOOD)] [[doc](https://opencood.readthedocs.io/en/latest/index.html)]
- **(People)** Siheng Chen@SJTU [[web](https://scholar.google.com/citations?hl=en&user=W_Q33RMAAAAJ&view_op=list_works&sortby=pubdate)], Chen Feng@NYU [[web](https://scholar.google.com/citations?hl=en&user=YeG8ZM0AAAAJ&view_op=list_works&sortby=pubdate)], Jiaqi Ma@UCLA [[web](https://scholar.google.com/citations?hl=en&user=S3cQz1AAAAAJ&view_op=list_works&sortby=pubdate)], Hang Qiu@Waymo [[web](https://hangqiu.github.io/)], Runsheng Xu@UCLA [[web](https://derrickxunu.github.io/)], Hao Xiang@UCLA [[web](https://xhwind.github.io/)], Yiming Li@NYU [[web](https://roboticsyimingli.github.io/)], Zixing Lei@SJTU [[web](https://chezacar.github.io/)], Yifan Lu@SJTU [[web](https://yifanlu0227.github.io/)]
- **(Workshop)** ICRA 2023 [[web](https://coperception.github.io/)], MFI 2022 [[web](https://coopermfi.github.io/)]
- **(Competition)** VIC3D Object Detection Challenge 清华AIR-百度Apollo车路协同自动驾驶算法挑战赛 [[info](https://aistudio.baidu.com/aistudio/competition/detail/522/0/introduction)]

### Typical Collaboration Modes:handshake::handshake::handshake:

![](mode.png)

### Published Benchmark Results:rocket::rocket::rocket:

- **V2XSet** (consider vehicles and infrastructures, pose error and time delay)

| Method | Ideal AP@0.7 | Noisy AP@0.7 |
| :-: | :-: | :-: |
| MPDA [ArXiv'22] | **73.4** | - |
| V2X-ViT [ECCV'22] | 71.2 | **61.4** |
| DiscoNet [NeurIPS'21] | 69.5 | 54.1 |
| F-Cooper [SEC'19] | 68.0 | 46.9 |
| V2VNet [ECCV'20] | 67.7 | 49.3 |
| AttFuse [ICRA'22] | 66.4 | 48.7 |
| Early Fusion (Upper Bound) | 71.0 | 38.4 |
| Late Fusion | 62.0 | 30.7 |
| No Fusion (Lower Bound) | 40.2 | 40.2 |

- **OPV2V**

| Method | Default AP@0.7 | Culver AP@0.7 |
| :-: | :-: | :-: |
| AdaFusion [WACV'22] | **85.6** | **79.0** |
| FuseBEVT [CoRL'22] | 85.2 | - |
| V2VAM [Arxiv'22] | 84.9 | 73.1 |
| CoBEVT [CoRL'22] | 83.6 | 74.8 |
| DiscoNet [NeurIPS'21] | 83.6 | - |
| V2X-ViT [ECCV'22] | 82.6 | 73.7 |
| V2VNet [ECCV'20] | 82.2 | 73.4 |
| FPV-RCNN [RAL'22] | 82.0 | 76.3 |
| AttFuse [ICRA'22] | 81.5 | 73.5 |
| MAMP [ArXiv'22] | 81.3 | - |
| F-Cooper [SEC'19] | 79.0 | 72.8 |
| V2VAM+LCRN [Arxiv'22] | 78.3 | 70.9 |
| CoAlign [Arxiv'22] | 74.3 | - |
| MASH [IROS'21] | 53.1 | - |
| Where2comm [NeurIPS'22] | 19.1 | - |
| Early Fusion (Upper Bound) | 80.0 | 69.6 |
| Late Fusion | 78.1 | 66.8 |
| No Fusion (Lower Bound) | 60.2 | 47.1 |

- The results above are directly borrowed from publicly accessible papers. Some of the results here might be somewhat unreasonable since they focus on specific issues and adopt different training settings. The best effort is tried to ensure that all the collected benchmark results are in the same testing settings (if provided).

### Reproduced Benchmark Results:sweat_drops::sweat_drops::sweat_drops:

- **OPV2V Default**

| Method | AP@0.7 | AP@0.5 | AP@0.3 |
| :-: | :-: | :-: | :-: |
| V2X-ViT [ECCV'22] |  |  |  |
| DiscoNet [NeurIPS'21] |  |  |  |
| V2VNet [ECCV'20] |  |  |  |
| When2com [CVPR'20] |  |  |  |
| AttFuse [ICRA'22] |  |  |  |
| F-Cooper [SEC'19] |  |  |  |
| Early Fusion (Upper Bound) |  |  |  |
| Late Fusion |  |  |  |
| No Fusion (Lower Bound) |  |  |  |

- **OPV2V Culver**

| Method | AP@0.7 | AP@0.5 | AP@0.3 |
| :-: | :-: | :-: | :-: |
| V2X-ViT [ECCV'22] |  |  |  |
| DiscoNet [NeurIPS'21] |  |  |  |
| V2VNet [ECCV'20] |  |  |  |
| When2com [CVPR'20] |  |  |  |
| AttFuse [ICRA'22] |  |  |  |
| F-Cooper [SEC'19] |  |  |  |
| Early Fusion (Upper Bound) |  |  |  |
| Late Fusion |  |  |  |
| No Fusion (Lower Bound) |  |  |  |

- **V2XSet Ideal**

| Method | AP@0.7 | AP@0.5 | AP@0.3 |
| :-: | :-: | :-: | :-: |
| V2X-ViT [ECCV'22] |  |  |  |
| DiscoNet [NeurIPS'21] |  |  |  |
| V2VNet [ECCV'20] |  |  |  |
| When2com [CVPR'20] |  |  |  |
| AttFuse [ICRA'22] |  |  |  |
| F-Cooper [SEC'19] |  |  |  |
| Early Fusion (Upper Bound) |  |  |  |
| Late Fusion |  |  |  |
| No Fusion (Lower Bound) |  |  |  |

- **V2XSet Noisy**

| Method | AP@0.7 | AP@0.5 | AP@0.3 |
| :-: | :-: | :-: | :-: |
| V2X-ViT [ECCV'22] |  |  |  |
| DiscoNet [NeurIPS'21] |  |  |  |
| V2VNet [ECCV'20] |  |  |  |
| When2com [CVPR'20] |  |  |  |
| AttFuse [ICRA'22] |  |  |  |
| F-Cooper [SEC'19] |  |  |  |
| Early Fusion (Upper Bound) |  |  |  |
| Late Fusion |  |  |  |
| No Fusion (Lower Bound) |  |  |  |

- **Joint Set**

| Method | AP@0.7 | AP@0.5 | AP@0.3 |
| :-: | :-: | :-: | :-: |
| V2X-ViT [ECCV'22] |  |  |  |
| DiscoNet [NeurIPS'21] |  |  |  |
| V2VNet [ECCV'20] |  |  |  |
| When2com [CVPR'20] |  |  |  |
| AttFuse [ICRA'22] |  |  |  |
| F-Cooper [SEC'19] |  |  |  |
| Early Fusion (Upper Bound) |  |  |  |
| Late Fusion |  |  |  |
| No Fusion (Lower Bound) |  |  |  |

- In Joint Set, the OPV2V test split (16 scenes), OPV2V test culver city split (4 scenes), OPV2V validation split (9 scenes), V2XSet test split (19 scenes) and V2XSet validation split (6 scenes) are combined together as a much larger evaluation dataset (totaling 54 different scenes) to allow more stable ranking. The evaluated models are trained on a joint set of OPV2V train split and V2XSet train split.
- For fair comparison, all methods adopt the same one-stage training strategy in ideal settings (i.e., no pose error or time delay), extra fusion modules (e.g., down-sampling convolution layers) of intermediate collaboration mode are simplified if not necessary to mitigate the concern about the actual performance gain.
- Some of the reproduced results are not satisfactory, cautious tuning and elaborate strategies are needed.



## :bookmark:Simulation Framework

### CVPR 2022:tada::tada::tada:

- **AutoCastSim** (AutoCastSim: An End-to-End Cooperative Perception and Collaborative Driving Simulation Framework) [[paper](https://arxiv.org/abs/2205.02222)] [[code](https://github.com/hangqiu/AutoCastSim)] [[project](https://utexas.app.box.com/v/coopernaut-dataset)]

### Preprint 2022

- **RLS** (Analyzing Infrastructure LiDAR Placement with Realistic LiDAR) [[paper](https://arxiv.org/abs/2211.15975)] [[code](https://github.com/PJLab-ADG/LiDARSimLib-and-Placement-Evaluation)] [~~project~~]
- **V2XP-ASG** (V2XP-ASG: Generating Adversarial Scenes for Vehicle-to-Everything Perception) [[paper](https://arxiv.org/abs/2209.13679)] [~~code~~] [~~project~~]



## :bookmark:Dataset

### CVPR 2022:tada::tada::tada:

- **DAIR-V2X** (DAIR-V2X: A Large-Scale Dataset for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper](https://arxiv.org/abs/2204.05575)] [[code](https://github.com/AIR-THU/DAIR-V2X)] [[project](https://thudair.baai.ac.cn/index)]

### NeurIPS 2022:tada::tada::tada:

- **CoPerception-UAVs** (Where2comm: Efficient Collaborative Perception via Spatial Confidence Maps) [[paper](https://arxiv.org/abs/2209.12836)] [[code](https://github.com/MediaBrain-SJTU/where2comm)] [[project](https://siheng-chen.github.io/dataset/coperception-uav/)]

### ECCV 2022:tada::tada::tada:

- **V2XSet** (V2X-ViT: Vehicle-to-Everything Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2203.10638)] [[code](https://github.com/DerrickXuNu/v2x-vit)] [[project](https://drive.google.com/drive/folders/1r5sPiBEvo8Xby-nMaWUTnJIPK6WhY1B6)]

### ICRA 2022

- **OPV2V** (OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication) [[paper](https://arxiv.org/abs/2109.07644)] [[code](https://github.com/DerrickXuNu/OpenCOOD)] [[project](https://mobility-lab.seas.ucla.edu/opv2v/)]

### ACCV 2022

- **DOLPHINS** (DOLPHINS: Dataset for Collaborative Perception Enabled Harmonious and Interconnected Self-Driving) [[paper](https://arxiv.org/abs/2207.07609)] [[code](https://github.com/explosion5/Dolphins)] [[project](https://dolphins-dataset.net/)]

### Preprint 2022

- **CARLA-3D** (Collaborative 3D Object Detection for Automatic Vehicle Systems via Learnable Communications) [[paper](https://arxiv.org/abs/2205.11849)] [~~code~~] [~~project~~]
- **DAIR-V2X-C** (Robust Collaborative 3D Object Detection in Presence of Pose Errors) [[paper](https://arxiv.org/abs/2211.07214)] [[code](https://github.com/yifanlu0227/CoAlign)] [[project](https://siheng-chen.github.io/dataset/dair-v2x-c-complemented/)]

### ICCV 2021:tada::tada::tada:

- **V2X-Sim** (V2X-Sim: Multi-Agent Collaborative Perception Dataset and Benchmark for Autonomous Driving) [[paper](https://arxiv.org/abs/2202.08449)] [[code](https://github.com/ai4ce/V2X-Sim/)] [[project](https://ai4ce.github.io/V2X-Sim/)]

### CVPR 2020:tada::tada::tada:

- **AirSim-MAP** (When2com: Multi-Agent Perception via Communication Graph Grouping) [[paper](https://arxiv.org/abs/2006.00176)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)] [[project](https://gtvault-my.sharepoint.com/:f:/g/personal/yliu3133_gatech_edu/Ett0G1_5YYdBpgojk0uWESgBi95dO79LkbYaKRhlBIkVJQ?e=vdjklb)]

### ECCV 2020:tada::tada::tada:

- **V2V-Sim** (V2VNet: Vehicle-to-Vehicle Communication for Joint Perception and Prediction) [[paper](https://arxiv.org/abs/2008.07519)] [~~code~~] [~~project~~]

### ICRA 2020

- **AirSim-CP** (Who2com: Collaborative Perception via Learnable Handshake Communication) [[paper](https://arxiv.org/abs/2003.09575)] [~~code~~] [~~project~~]



## :bookmark:Method

### CVPR 2022:tada::tada::tada:

- **Coopernaut** (COOPERNAUT: End-to-End Driving with Cooperative Perception for Networked Vehicles) [[paper](https://arxiv.org/abs/2205.02222)] [[code](https://github.com/UT-Austin-RPL/Coopernaut)]
  - Mode: Intermediate Collaboration
  - Dataset: AutoCastSim (a simulation framework)
  - Task: Policy Learning

### NeurIPS 2022:tada::tada::tada:

- **Where2comm** (Where2comm: Efficient Collaborative Perception via Spatial Confidence Maps) [[paper](https://arxiv.org/abs/2209.12836)] [[code](https://github.com/MediaBrain-SJTU/where2comm)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2X-Sim, DAIR-V2X, CoPerception-UAVs
  - Task: 3D Detection

### ECCV 2022:tada::tada::tada:

- **SyncNet** (Latency-Aware Collaborative Perception) [[paper](https://arxiv.org/abs/2207.08560)] [[code](https://github.com/MediaBrain-SJTU/SyncNet)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: 3D Detection
- **V2X-ViT** (V2X-ViT: Vehicle-to-Everything Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2203.10638)] [[code](https://github.com/DerrickXuNu/v2x-vit)]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet
  - Task: 3D Detection

### CoRL 2022:tada::tada::tada:

- **CoBEVT** (CoBEVT: Cooperative Bird's Eye View Semantic Segmentation with Sparse Transformers) [[paper](https://arxiv.org/abs/2207.02202)] [[code](https://github.com/DerrickXuNu/CoBEVT)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: 2D Segmentation, 3D Detection
- **STAR** (Multi-Robot Scene Completion: Towards Task-Agnostic Collaborative Perception) [[paper](https://openreview.net/forum?id=hW0tcXOJas2)] [[code](https://github.com/coperception/star)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: 2D Segmentation, 3D Detection

### IJCAI 2022

- **IA-RCP** (Robust Collaborative Perception against Communication Interruption) [[paper](https://learn-to-race.org/workshop-ai4ad-ijcai2022/papers.html)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: 3D Detection

### MM 2022

- **CRCNet** (Complementarity-Enhanced and Redundancy-Minimized Collaboration Network for Multi-agent Perception) [[paper](https://dl.acm.org/doi/abs/10.1145/3503161.3548197)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: 3D Detection

### WACV 2022

- **AdaFusion** (Adaptive Feature Fusion for Cooperative Perception Using LiDAR Point Clouds) [[paper](https://arxiv.org/abs/2208.00116)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: 3D Detection

### ICRA 2022

- **AttFuse** (OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication) [[paper](https://arxiv.org/abs/2109.07644)] [[code](https://github.com/DerrickXuNu/OpenCOOD)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: 3D Detection
- **MP-Pose** (Multi-Robot Collaborative Perception with Graph Neural Networks) [[paper](https://arxiv.org/abs/2201.01760)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-MAP
  - Task: 2D Segmentation

### Preprint 2022

- **CoAlign** (Robust Collaborative 3D Object Detection in Presence of Pose Errors) [[paper](https://arxiv.org/abs/2211.07214)] [[code](https://github.com/yifanlu0227/CoAlign)]
  - Mode: Intermediate Collaboration, Late Collaboration
  - Dataset: OPV2V, V2X-Sim, DAIR-V2X
  - Task: 3D Detection
- **CO^3** (CO^3: Cooperative Unsupervised 3D Representation Learning for Autonomous Driving) [[paper](https://arxiv.org/abs/2206.04028)] [[code](https://github.com/Runjian-Chen/CO3)]
  - Mode: Intermediate Collaboration (for contrastive learning)
  - Dataset: DAIR-V2X
  - Task: Representation Learning
- **Double-M Quantification** (Uncertainty Quantification of Collaborative Detection for Self-Driving) [[paper](https://arxiv.org/abs/2209.08162)] [[code](https://github.com/coperception/double-m-quantification)]
  - Mode: Early Collaboration, Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: 3D Detection
- **ICP&OT** (An Efficient and Robust Object-Level Cooperative Perception Framework for Connected and Automated Driving) [[paper](https://arxiv.org/abs/2210.06289)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: OPV2V
  - Task: 3D Detection
- **Learn2com** (Collaborative 3D Object Detection for Automatic Vehicle Systems via Learnable Communications) [[paper](https://arxiv.org/abs/2205.11849)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: CARLA-3D
  - Task: 3D Detection
- **MAMP** (Model-Agnostic Multi-Agent Perception Framework) [[paper](https://arxiv.org/abs/2203.13168)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: OPV2V
  - Task: 3D Detection
- **MPDA** (Bridging the Domain Gap for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2210.08451)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet
  - Task: 3D Detection
- **V2VAM+LCRN** (Learning for Vehicle-to-Vehicle Cooperative Perception under Lossy Communication) [[paper](https://arxiv.org/abs/2212.08273)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: 3D Detection

### NeurIPS 2021:tada::tada::tada:

- **DiscoNet** (Learning Distilled Collaboration Graph for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2111.00643)] [[code](https://github.com/ai4ce/DiscoNet)]
  - Mode: Early Collaboration (teacher model), Intermediate Collaboration (student model)
  - Dataset: V2X-Sim
  - Task: 3D Detection

### ICCV 2021:tada::tada::tada:

- **Adversarial V2V** (Adversarial Attacks On Multi-Agent Communication) [[paper](https://arxiv.org/abs/2101.06560)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: Adversarial Attack

### IROS 2021

- **MASH** (Overcoming Obstructions via Bandwidth-Limited Multi-Agent Spatial Handshaking) [[paper](https://arxiv.org/abs/2107.00771)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: Unkown
  - Task: 2D Segmentation

### CVPR 2020:tada::tada::tada:

- **When2com** (When2com: Multi-Agent Perception via Communication Graph Grouping) [[paper](https://arxiv.org/abs/2006.00176)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-MAP
  - Task: 2D Segmentation, 3D Classification

### ECCV 2020:tada::tada::tada:

- **V2VNet** (V2VNet: Vehicle-to-Vehicle Communication for Joint Perception and Prediction) [[paper](https://arxiv.org/abs/2008.07519)] [[code](https://github.com/coperception/coperception)]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: 3D Detection, Motion Forecasting

### CoRL 2020:tada::tada::tada:

- **Robust V2V** (Learning to Communicate and Correct Pose Errors) [[paper](https://arxiv.org/abs/2011.05289)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: 3D Detection, Motion Forecasting

### ICRA 2020

- **Who2com** (Who2com: Collaborative Perception via Learnable Handshake Communication) [[paper](https://arxiv.org/abs/2003.09575)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-CP (has an asynchronous issue between views)
  - Task: 2D Segmentation