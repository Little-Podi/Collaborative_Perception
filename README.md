# Collaborative Perception

This repository is a paper digest of recent advances in **collaborative** / **cooperative** / **multi-agent** perception for **V2I** / **V2V** / **V2X** autonomous driving scenario. Papers are listed in alphabetical order of the first character.

### :link:Jump to:
- ### [[Method and Framework](https://github.com/Little-Podi/Collaborative_Perception#bookmarkmethod-and-framework)]
- ### [[Dataset and Simulator](https://github.com/Little-Podi/Collaborative_Perception#bookmarkdataset-and-simulator)]

Note: I find it hard to fairly compare all methods on each benchmark since some published results are obtained without specified training and testing settings, or even modified model architectures. In fact, many works evaluate all baselines under their own settings and report them. Therefore, it is probably to find inconsistency between papers. Hence, I discard the collection and reproducton of all the benchmarks in a previous update. If you are interested, you can find plenty of results in [this archived version](https://github.com/Little-Podi/Collaborative_Perception/tree/1be25908aea0a9f635ff4852b3a90729cf2b6aac).



## :star2:Recommendation

### Helpful Learning Resource:thumbsup::thumbsup::thumbsup:

- **(Survey)** Collaborative Perception for Connected and Autonomous Driving: Challenges, Possible Solutions and Opportunities [[paper](https://arxiv.org/abs/2401.01544)], V2X Cooperative Perception for Autonomous Driving: Recent Advances and Challenges [[paper](https://arxiv.org/abs/2310.03525)], Towards Vehicle-to-Everything Autonomous Driving: A Survey on Collaborative Perception [[paper](https://arxiv.org/abs/2308.16714)], Collaborative Perception in Autonomous Driving: Methods, Datasets and Challenges [[paper](https://arxiv.org/abs/2301.06262)], A Survey and Framework of Cooperative Perception: From Heterogeneous Singleton to Hierarchical Cooperation [[paper](https://arxiv.org/abs/2208.10590)]
- **(Talk)** The Ultimate Solution for L4 Autonomous Driving [[video](https://youtu.be/cyNxemm4Ujg)], All You Need to Know about Self-Driving [[video](https://youtu.be/WUDxYn7QtJU)], When Vision Transformers Meet Cooperative Perception [[video](https://youtu.be/rLAU4eqoOIU)], Scene Understanding beyond the Visible [[video](https://youtu.be/oz0AnmJZCR4)], Robust Collaborative Perception against Communication Interruption [[video](https://youtu.be/3cIWpMrsyeE)], Collaborative and Adversarial 3D Perception for Autonomous Driving [[video](https://youtu.be/W-AONQMfGi0)], Vehicle-to-Vehicle Communication for Self-Driving [[video](https://youtu.be/oikdOpmIoc4)], Adversarial Robustness for Self-Driving [[video](https://youtu.be/8uBFXzyII5Y)], L4感知系统的终极形态：协同驾驶 [[video](https://youtu.be/NvixMEDHht4)], CoBEVFlow-解决车-车/路协同感知的时序异步问题 [[video](https://youtu.be/IBTgalAjye8)], 新一代协作感知Where2comm减少通信带宽十万倍 [[video](https://youtu.be/i5coMk4hkuk)], 从任务相关到任务无关的多机器人协同感知 [[video](https://course.zhidx.com/c/MDlkZjcyZDgwZWI4ODBhOGQ4MzM=)], 协同自动驾驶：仿真与感知 [[video](https://course.zhidx.com/c/MmQ1YWUyMzM1M2I3YzVlZjE1NzM=)], 基于群体协作的超视距态势感知 [[video](https://www.koushare.com/video/videodetail/33015)]
- **(Library)** V2Xverse: A Codebase for V2X-Based Collaborative End2End Autonomous Driving [[code](https://github.com/CollaborativePerception/V2Xverse)] [[doc](https://collaborativeperception.github.io/V2Xverse)], HEAL: An Extensible Framework for Open Heterogeneous Collaborative Perception [[code](https://github.com/yifanlu0227/HEAL)] [[doc](https://huggingface.co/yifanlu/HEAL)], OpenCOOD: Open Cooperative Detection Framework for Autonomous Driving [[code](https://github.com/DerrickXuNu/OpenCOOD)] [[doc](https://opencood.readthedocs.io/en/latest/index.html)], CoPerception: SDK for Collaborative Perception [[code](https://github.com/coperception/coperception)] [[doc](https://coperception.readthedocs.io/en/latest)], OpenCDA: Simulation Tool Integrated with Prototype Cooperative Driving Automation [[code](https://github.com/ucla-mobility/OpenCDA)] [[doc](https://opencda-documentation.readthedocs.io/en/latest)]
- **(People)** Runsheng Xu@UCLA [[web](https://derrickxunu.github.io)], Hao Xiang@UCLA [[web](https://xhwind.github.io)], Yiming Li@NYU [[web](https://yimingli-page.github.io)], Zixing Lei@SJTU [[web](https://chezacar.github.io)], Yifan Lu@SJTU [[web](https://yifanlu0227.github.io)], Siqi Fan@THU [[web](https://leofansq.github.io)], Hang Qiu@Waymo [[web](https://hangqiu.github.io)], Dian Chen@UT Austin [[web](https://www.cs.utexas.edu/~dchen)], Yen-Cheng Liu@GaTech [[web](https://ycliu93.github.io)], Tsun-Hsuan Wang@MIT [[web](https://zswang666.github.io)]
- **(Workshop)** CoPerception@ICRA'23 [[web](https://coperception.github.io)], ScalableAD@ICRA'23 [[web](https://sites.google.com/view/icra2023av/home)]
- **(Background)** Current Approaches and Future Directions for Point Cloud Object Detection in Intelligent Agents [[video](https://youtu.be/xFFCQVwYeec)], 3D Object Detection for Autonomous Driving: A Review and New Outlooks [[paper](https://arxiv.org/abs/2206.09474)], DACOM: Learning Delay-Aware Communication for Multi-Agent Reinforcement Learning [[video](https://youtu.be/YBgW2oA_n3k)], A Survey of Multi-Agent Reinforcement Learning with Communication [[paper](https://arxiv.org/abs/2203.08975)]

### Typical Collaboration Modes:handshake::handshake::handshake:

![](mode.png)

### Possible Optimization Directions:fire::fire::fire:

![](direction.png)



## :bookmark:Method and Framework

Note: {Related} denotes that it is not a pure collaborative perception paper but has related content.

### Selected Preprint

- **AR2VP** (Dynamic V2X Autonomous Perception from Road-to-Vehicle Vision) [[paper](https://arxiv.org/abs/2310.19113)] [[code](https://github.com/tjy1423317192/AP2VP)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Segmentation
  - Input: Point Cloud
- **CMP** (CMP: Cooperative Motion Prediction with Multi-Agent Communication) [[paper](https://arxiv.org/abs/2403.17916)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Forecasting
  - Input: Point Cloud
- **CoBEVFusion** (CoBEVFusion: Cooperative Perception with LiDAR-Camera Bird's-Eye View Fusion) [[paper](https://arxiv.org/abs/2310.06008)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Segmentation, Detection
  - Input: RGB Image, Point Cloud
- **CoBEVGlue** (Self-Localized Collaborative Perception) [[paper](https://arxiv.org/abs/2406.12712)] [[code](https://github.com/VincentNi0107/CoBEVGlue)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2V4Real, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **CoDriving** (Towards Collaborative Autonomous Driving: Simulation Platform and End-to-End System) [[paper](https://arxiv.org/abs/2404.09496)] [[code](https://github.com/CollaborativePerception/V2Xverse)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2V4Real, V2X-Sim, DAIR-V2X
  - Task: Planning
  - Input: RGB Image, Point Cloud
- **CoDrivingLLM** (Towards Interactive and Learnable Cooperative Driving Automation: A Large Language Model-Driven Decision-making Framework) [~~paper~~] [[code](https://github.com/FanGShiYuu/CoDrivingLLM)]
  - Mode:
  - Dataset:
  - Task: Planning
  - Input:
- **Coopre** (CooPre: Cooperative Pretraining for V2X Cooperative Perception)
  - Mode: Early Collaboration, Intermediate Collaboration
  - Dataset: OPV2V, V2V4Real, V2X-Real
  - Task: Detection
  - Input: Point Cloud
- **CTCE** (Leveraging Temporal Contexts to Enhance Vehicle-Infrastructure Cooperative Perception) [[paper](https://arxiv.org/abs/2408.10531)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X-Seq, V2X-Sim
  - Task: Detection
  - Input: RGB Image
- **MOT-CUP** (Collaborative Multi-Object Tracking with Conformal Uncertainty Propagation) [[paper](https://arxiv.org/abs/2303.14346)] [[code](https://github.com/susanbao/mot_cup)]
  - Mode: Early Collaboration, Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Tracking
  - Input: Point Cloud
- **PragComm** (Pragmatic Communication in Multi-Agent Collaborative Perception) [[paper](https://arxiv.org/abs/2401.12694)] [[code](https://github.com/PhyllisH/PragComm)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2X-Sim, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **QUEST** (QUEST: Query Stream for Vehicle-Infrastructure Cooperative Perception) [[paper](https://arxiv.org/abs/2308.01804)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X-Seq
  - Task: Detection
  - Input: RGB Image
- **RCDN** (RCDN: Towards Robust Camera-Insensitivity Collaborative Perception via Dynamic Feature-Based 3D Neural Modeling) [[paper](https://arxiv.org/abs/2405.16868)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V-N
  - Task: Segmentation
  - Input: RGB Image
- **SiCP** (SiCP: Simultaneous Individual and Cooperative Perception for 3D Object Detection in Connected and Automated Vehicles) [[paper](https://arxiv.org/abs/2312.04822)] [[code](https://github.com/DarrenQu/SiCP)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Detection
  - Input: Point Cloud
- **UniV2X** (End-to-End Autonomous Driving through V2X Cooperation) [[paper](https://arxiv.org/abs/2404.00717)] [[code](https://github.com/AIR-THU/UniV2X)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X
  - Task: Planning, Occupancy, Segmentation, Tracking
  - Input: RGB Image
- **VIMI** (VIMI: Vehicle-Infrastructure Multi-View Intermediate Fusion for Camera-Based 3D Object Detection) [[paper](https://arxiv.org/abs/2303.10975)] [[code](https://github.com/Bosszhe/VIMI)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X
  - Task: Detection
  - Input: RGB Image
- **V2X-DGW** (V2X-DGW: Domain Generalization for Multi-Agent Perception under Adverse Weather Conditions) [[paper](https://arxiv.org/abs/2403.11371)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V-w, V2XSet-w
  - Task: Detection
  - Input: Point Cloud
- **V2X-Graph** (Learning Cooperative Trajectory Representations for Motion Forecasting) [[paper](https://arxiv.org/abs/2311.00371)] [[code](https://github.com/AIR-THU/V2X-Graph)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X-Seq, DAIR-V2X-Traj
  - Task: Forecasting
  - Input: Vector Map
- **V2X-M2C** (V2X-M2C: Efficient Multi-Module Collaborative Perception with Two Connections) [[paper](https://arxiv.org/abs/2407.11546)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet
  - Task: Detection
  - Input: Point Cloud
- **V2X-PC** (V2X-PC: Vehicle-to-Everything Collaborative Perception via Point Cluster) [[paper](https://arxiv.org/abs/2403.16635)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud

### CVPR 2024

- **CoHFF** (Collaborative Semantic Occupancy Prediction with Hybrid Feature Fusion in Connected Automated Vehicles) [[paper](https://arxiv.org/abs/2402.07635)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V+
  - Task: Occupancy, Segmentation, Detection
  - Input: RGB Image
- **CoopDet3D** (TUMTraf V2X Cooperative Perception Dataset) [[paper](https://arxiv.org/abs/2403.01316)] [[code](https://github.com/tum-traffic-dataset/coopdet3d)]
  - Mode: Intermediate Collaboration
  - Dataset: TUMTraf-V2X
  - Task: Detection
  - Input: RGB Image, Point Cloud
- **CodeFilling** (Communication-Efficient Collaborative Perception via Information Filling with Codebook) [[paper](https://arxiv.org/abs/2405.04966)] [[code](https://github.com/PhyllisH/CodeFilling)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X, OPV2VH+
  - Task: Detection
  - Input: RGB Image, Point Cloud
- **MRCNet** Multi-Agent Collaborative Perception via Motion-Aware Robust Communication Network [[paper](https://openaccess.thecvf.com/content/CVPR2024/html/Hong_Multi-agent_Collaborative_Perception_via_Motion-aware_Robust_Communication_Network_CVPR_2024_paper.html)] [[code](https://github.com/IndigoChildren/collaborative-perception-MRCNet)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet, V2X-Sim
  - Task: Detection
  - Input: Point Cloud

### ICLR 2024

- **HEAL** (An Extensible Framework for Open Heterogeneous Collaborative Perception) [[paper&review](https://openreview.net/forum?id=KkrDUGIASk)] [[code](https://github.com/yifanlu0227/HEAL)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V-H, DAIR-V2X
  - Task: Detection
  - Input: RGB Image, Point Cloud

### AAAI 2024

- **CMiMC** (What Makes Good Collaborative Views? Contrastive Mutual Information Maximization for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2403.10068)] [[code](https://github.com/77SWF/CMiMC)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud
- **DI-V2X** (DI-V2X: Learning Domain-Invariant Representation for Vehicle-Infrastructure Collaborative 3D Object Detection) [[paper](https://arxiv.org/abs/2312.15742)] [[code](https://github.com/Serenos/DI-V2X)]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **V2XFormer** (DeepAccident: A Motion and Accident Prediction Benchmark for V2X Autonomous Driving) [[paper](https://arxiv.org/abs/2304.01168)] [[code](https://github.com/tianqi-wang1996/DeepAccident)]
  - Mode: Intermediate Collaboration
  - Dataset: DeepAccident
  - Task: Detection, Forecasting
  - Input: RGB Image

### WACV 2024

- **MACP** (MACP: Efficient Model Adaptation for Cooperative Perception) [[paper](https://arxiv.org/abs/2310.16870)] [[code](https://github.com/PurdueDigitalTwin/MACP)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2V4Real
  - Task: Detection
  - Input: Point Cloud

### ICRA 2024

- **FreeAlign** (Robust Collaborative Perception without External Localization and Clock Devices) [[paper](https://arxiv.org/abs/2405.02965)] [[code](https://github.com/MediaBrain-SJTU/FreeAlign)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud

### CVPR 2023

- {Related} **BEVHeight** (BEVHeight: A Robust Framework for Vision-Based Roadside 3D Object Detection) [[paper](https://arxiv.org/abs/2303.08498)] [[code](https://github.com/ADLab-AutoDrive/BEVHeight)]
  - Mode: No Collaboration (only infrastructure data)
  - Dataset: DAIR-V2X, V2X-Sim
  - Task: Detection
  - Input: RGB Image
- **CoCa3D** (Collaboration Helps Camera Overtake LiDAR in 3D Detection) [[paper](https://arxiv.org/abs/2303.13560)] [[code](https://github.com/MediaBrain-SJTU/CoCa3D)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V+, DAIR-V2X, CoPerception-UAV+
  - Task: Detection
  - Input: RGB Image
- **FF-Tracking** (V2X-Seq: The Large-Scale Sequential Dataset for the Vehicle-Infrastructure Cooperative Perception and Forecasting) [[paper](https://arxiv.org/abs/2305.05938)] [[code](https://github.com/AIR-THU/DAIR-V2X-Seq)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X-Seq
  - Task: Tracking
  - Input: Point Cloud

### NeurIPS 2023

- **CoBEVFlow** (Robust Asynchronous Collaborative 3D Detection via Bird's Eye View Flow) [[paper&review](https://openreview.net/forum?id=UHIDdtxmVS)] [[code](https://github.com/MediaBrain-SJTU/CoBEVFlow)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X, IRV2V
  - Task: Detection
  - Input: Point Cloud
- **FFNet** (Flow-Based Feature Fusion for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper&review](https://openreview.net/forum?id=gsglrhvQxX)] [[code](https://github.com/haibao-yu/FFNet-VIC3D)]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **How2comm** (How2comm: Communication-Efficient and Collaboration-Pragmatic Multi-Agent Perception) [[paper&review](https://openreview.net/forum?id=Dbaxm9ujq6)] [[code](https://github.com/ydk122024/How2comm)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud

### ICCV 2023

- **CORE** (CORE: Cooperative Reconstruction for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2307.11514)] [[code](https://github.com/zllxot/CORE)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Segmentation, Detection
  - Input: Point Cloud
- **HM-ViT** (HM-ViT: Hetero-Modal Vehicle-to-Vehicle Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2304.10628)] [[code](https://github.com/XHwind/HM-ViT)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Detection
  - Input: RGB Image, Point Cloud
- **ROBOSAC** (Among Us: Adversarially Robust Collaborative Perception by Consensus) [[paper](https://arxiv.org/abs/2303.09495)] [[code](https://github.com/coperception/ROBOSAC)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud
- **SCOPE** (Spatio-Temporal Domain Awareness for Multi-Agent Collaborative Perception) [[paper](https://arxiv.org/abs/2307.13929)] [[code](https://github.com/starfdu1418/SCOPE)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet, DAIR-V2X
  - Task: Segmentation, Detection
  - Input: Point Cloud
- **TransIFF** (TransIFF: An Instance-Level Feature Fusion Framework for Vehicle-Infrastructure Cooperative 3D Detection with Transformers) [[paper](https://openaccess.thecvf.com/content/ICCV2023/html/Chen_TransIFF_An_Instance-Level_Feature_Fusion_Framework_for_Vehicle-Infrastructure_Cooperative_3D_ICCV_2023_paper.html)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **UMC** (UMC: A Unified Bandwidth-Efficient and Multi-Resolution Based Collaborative Perception Framework) [[paper](https://arxiv.org/abs/2303.12400)] [[code](https://github.com/ispc-lab/UMC)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2X-Sim
  - Task: Detection
  - Input: Point Cloud

### ICLR 2023

- {Related} **CO3** (CO3: Cooperative Unsupervised 3D Representation Learning for Autonomous Driving) [[paper&review](https://openreview.net/forum?id=QUaDoIdgo0)] [[code](https://github.com/Runjian-Chen/CO3)]
  - Mode: Early Collaboration (for contrastive learning)
  - Dataset: DAIR-V2X
  - Task: Representation Learning
  - Input: Point Cloud

### CoRL 2023

- **BM2CP** {BM2CP: Efficient Collaborative Perception with LiDAR-Camera Modalities} [[paper&review](https://openreview.net/forum?id=uJqxFjF1xWp)] [[code](https://github.com/byzhaoAI/BM2CP)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, DAIR-V2X
  - Task: Detection
  - Input: RGB Image, Point Cloud

### MM 2023

- **DUSA** (DUSA: Decoupled Unsupervised Sim2Real Adaptation for Vehicle-to-Everything Collaborative Perception) [[paper](https://arxiv.org/abs/2310.08117)] [[code](https://github.com/refkxh/DUSA)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- **FeaCo** (FeaCo: Reaching Robust Feature-Level Consensus in Noisy Pose Conditions) [[paper](https://dl.acm.org/doi/abs/10.1145/3581783.3611880)] [[code](https://github.com/jmgu0212/FeaCo)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2V4Real
  - Task: Detection
  - Input: Point Cloud
- **What2comm** (What2comm: Towards Communication-Efficient Collaborative Perception via Feature Decoupling) [[paper](https://dl.acm.org/doi/abs/10.1145/3581783.3611699)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, V2XSet, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud

### WACV 2023

- **AdaFusion** (Adaptive Feature Fusion for Cooperative Perception Using LiDAR Point Clouds) [[paper](https://arxiv.org/abs/2208.00116)] [[code](https://github.com/DonghaoQiao/Adaptive-Feature-Fusion-for-Cooperative-Perception)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, CODD
  - Task: Detection
  - Input: Point Cloud

### ICRA 2023

- **CoAlign** (Robust Collaborative 3D Object Detection in Presence of Pose Errors) [[paper](https://arxiv.org/abs/2211.07214)] [[code](https://github.com/yifanlu0227/CoAlign)]
  - Mode: Intermediate Collaboration, Late Collaboration
  - Dataset: OPV2V, V2X-Sim, DAIR-V2X
  - Task: Detection
  - Input: Point Cloud
- {Related} **DMGM** (Deep Masked Graph Matching for Correspondence Identification in Collaborative Perception) [[paper](https://arxiv.org/abs/2303.07555)] [[code](https://github.com/gaopeng5/DMGM)]
  - Mode: Intermediate Collaboration
  - Dataset: CAD
  - Task: Correspondence Identification
  - Input: RGBD Image
- **Double-M Quantification** (Uncertainty Quantification of Collaborative Detection for Self-Driving) [[paper](https://arxiv.org/abs/2209.08162)] [[code](https://github.com/coperception/double-m-quantification)]
  - Mode: Early Collaboration, Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud
- **MAMP** (Model-Agnostic Multi-Agent Perception Framework) [[paper](https://arxiv.org/abs/2203.13168)] [[code](https://github.com/DerrickXuNu/model_anostic)]
  - Mode: Late Collaboration
  - Dataset: OPV2V
  - Task: Detection
  - Input: Point Cloud
- **MATE** (Communication-Critical Planning via Multi-Agent Trajectory Exchange) [[paper](https://arxiv.org/abs/2303.06080)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: AutoCastSim (simulator), CoBEV-Sim (simulator)
  - Task: Planning
  - Input: Point Cloud
- **MPDA** (Bridging the Domain Gap for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2210.08451)] [[code](https://github.com/DerrickXuNu/MPDA)]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet
  - Task: Detection
  - Input: Point Cloud
- **WNT** (We Need to Talk: Identifying and Overcoming Communication-Critical Scenarios for Self-Driving) [[paper](https://arxiv.org/abs/2305.04352)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: CoBEV-Sim (simulator)
  - Task: Planning
  - Input: Point Cloud

### CVPR 2022

- **Coopernaut** (COOPERNAUT: End-to-End Driving with Cooperative Perception for Networked Vehicles) [[paper](https://arxiv.org/abs/2205.02222)] [[code](https://github.com/UT-Austin-RPL/Coopernaut)]
  - Mode: Intermediate Collaboration
  - Dataset: AutoCastSim (simulator)
  - Task: Planning
  - Input: Point Cloud
- {Related} **LAV** (Learning from All Vehicles) [[paper](https://arxiv.org/abs/2203.11934)] [[code](https://github.com/dotchen/LAV)]
  - Mode: Late Collaboration (for training)
  - Dataset: CARLA (simulator)
  - Task: Planning, Detection (auxiliary supervision), Segmentation (auxiliary supervision)
  - Input: RGB Image, Point Cloud
- **TCLF** (DAIR-V2X: A Large-Scale Dataset for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper](https://arxiv.org/abs/2204.05575)] [[code](https://github.com/AIR-THU/DAIR-V2X)]
  - Mode: Late Collaboration
  - Dataset: DAIR-V2X
  - Task: Detection
  - Input: RGB Image, Point Cloud

### NeurIPS 2022

- **Where2comm** (Where2comm: Efficient Collaborative Perception via Spatial Confidence Maps) [[paper&review](https://openreview.net/forum?id=dLL4KXzKUpS)] [[code](https://github.com/MediaBrain-SJTU/where2comm)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, DAIR-V2X, V2X-Sim, CoPerception-UAV
  - Task: Detection
  - Input: Point Cloud

### ECCV 2022

- **SyncNet** (Latency-Aware Collaborative Perception) [[paper](https://arxiv.org/abs/2207.08560)] [[code](https://github.com/MediaBrain-SJTU/SyncNet)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud
- **V2X-ViT** (V2X-ViT: Vehicle-to-Everything Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2203.10638)] [[code](https://github.com/DerrickXuNu/v2x-vit)]
  - Mode: Intermediate Collaboration
  - Dataset: V2XSet
  - Task: Detection
  - Input: Point Cloud

### CoRL 2022

- **CoBEVT** (CoBEVT: Cooperative Bird's Eye View Semantic Segmentation with Sparse Transformers) [[paper&review](https://openreview.net/forum?id=PAFEQQtDf8s)] [[code](https://github.com/DerrickXuNu/CoBEVT)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V, nuScenes
  - Task: Segmentation, Detection
  - Input: RGB Image, Point Cloud
- **STAR** (Multi-Robot Scene Completion: Towards Task-Agnostic Collaborative Perception) [[paper&review](https://openreview.net/forum?id=hW0tcXOJas2)] [[code](https://github.com/coperception/star)]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Segmentation, Detection
  - Input: Point Cloud

### IJCAI 2022

- **IA-RCP** (Robust Collaborative Perception against Communication Interruption) [[paper](https://learn-to-race.org/workshop-ai4ad-ijcai2022/papers.html)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud

### MM 2022

- **CRCNet** (Complementarity-Enhanced and Redundancy-Minimized Collaboration Network for Multi-agent Perception) [[paper](https://dl.acm.org/doi/abs/10.1145/3503161.3548197)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud

### ICRA 2022

- **AttFuse** (OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication) [[paper](https://arxiv.org/abs/2109.07644)] [[code](https://github.com/DerrickXuNu/OpenCOOD)]
  - Mode: Intermediate Collaboration
  - Dataset: OPV2V
  - Task: Detection
  - Input: Point Cloud
- **MP-Pose** (Multi-Robot Collaborative Perception with Graph Neural Networks) [[paper](https://arxiv.org/abs/2201.01760)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-MAP
  - Task: Segmentation
  - Input: RGB Image

### NeurIPS 2021

- **DiscoNet** (Learning Distilled Collaboration Graph for Multi-Agent Perception) [[paper&review](https://openreview.net/forum?id=ZRcjSOmYraB)] [[code](https://github.com/ai4ce/DiscoNet)]
  - Mode: Early Collaboration (teacher model), Intermediate Collaboration (student model)
  - Dataset: V2X-Sim
  - Task: Detection
  - Input: Point Cloud

### ICCV 2021

- **Adversarial V2V** (Adversarial Attacks On Multi-Agent Communication) [[paper](https://arxiv.org/abs/2101.06560)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: Adversarial Attack
  - Input: Point Cloud

### IROS 2021

- **MASH** (Overcoming Obstructions via Bandwidth-Limited Multi-Agent Spatial Handshaking) [[paper](https://arxiv.org/abs/2107.00771)] [[code](https://github.com/yifanlu0227/CoAlign)]
  - Mode: Late Collaboration
  - Dataset: AirSim
  - Task: Segmentation
  - Input: RGB Image

### CVPR 2020

- **When2com** (When2com: Multi-Agent Perception via Communication Graph Grouping) [[paper](https://arxiv.org/abs/2006.00176)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-MAP
  - Task: Segmentation, Classification
  - Input: RGB Image

### ECCV 2020

- **DSDNet** (DSDNet: Deep Structured Self-Driving Network) [[paper](https://arxiv.org/abs/2008.06041)] [~~code~~]
  - Mode: Late Collaboration
  - Dataset: nuScenes, CARLA (simulator), ATG4D
  - Task: Planning
  - Input: Point Cloud
- **V2VNet** (V2VNet: Vehicle-to-Vehicle Communication for Joint Perception and Prediction) [[paper](https://arxiv.org/abs/2008.07519)] [[code](https://github.com/DerrickXuNu/OpenCOOD)]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: Detection, Forecasting
  - Input: Point Cloud

### CoRL 2020

- **Robust V2V** (Learning to Communicate and Correct Pose Errors) [[paper](https://arxiv.org/abs/2011.05289)] [[code](https://github.com/yifanlu0227/CoAlign)]
  - Mode: Intermediate Collaboration
  - Dataset: V2V-Sim (not publicly available)
  - Task: Detection, Forecasting
  - Input: Point Cloud

### ICRA 2020

- **Who2com** (Who2com: Collaborative Perception via Learnable Handshake Communication) [[paper](https://arxiv.org/abs/2003.09575)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim-CP (has an asynchronous issue between views)
  - Task: Segmentation
  - Input: RGB Image
- **MAIN** (Enhancing Multi-Robot Perception via Learned Data Association) [[paper](https://arxiv.org/abs/2107.00769)] [~~code~~]
  - Mode: Intermediate Collaboration
  - Dataset: AirSim
  - Task: Segmentation
  - Input: RGB Image



## :bookmark:Dataset and Simulator

Note: {Real} denotes that the sensor data is obtained by real-world collection instead of simulation.

### Selected Preprint

- {Real} **InScope** (InScope: A New Real-world 3D Infrastructure-side Collaborative Perception Dataset for Open Traffic Scenarios) [[paper](https://arxiv.org/abs/2407.21581)] [[code](https://github.com/xf-zh/InScope)] [~~project~~]
- **Multi-V2X** (Multi-V2X: A Large Scale Multi-modal Multi-penetration-rate Dataset for Cooperative Perception) [[paper](https://arxiv.org/abs/2409.04980)] [[code](https://github.com/RadetzkyLi/Multi-V2X)] [~~project~~]
- **OPV2V-N** (RCDN: Towards Robust Camera-Insensitivity Collaborative Perception via Dynamic Feature-based 3D Neural Modeling) [[paper](https://arxiv.org/abs/2405.16868)] [~~code~~] [~~project~~]
- {Real} **V2X-Real** (V2X-Real: a Large-Scale Dataset for Vehicle-to-Everything Cooperative Perception) [[paper](https://arxiv.org/abs/2403.16034)] [~~code~~] [~~project~~]
- {Real} **DAIR-V2X-Traj** (Learning Cooperative Trajectory Representations for Motion Forecasting) [[paper](https://arxiv.org/abs/2311.00371)] [[code](https://github.com/AIR-THU/V2X-Graph)] [[project](https://thudair.baai.ac.cn/index)]

### CVPR 2024

- {Real} **HoloVIC** (HoloVIC: Large-Scale Dataset and Benchmark for Multi-Sensor Holographic Intersection and Vehicle-Infrastructure Cooperative) [[paper](https://arxiv.org/abs/2403.02640)] [~~code~~] [[project](https://holovic.net)]
- {Real} **Open Mars Dataset** (Multiagent Multitraversal Multimodal Self-Driving: Open MARS Dataset) [[code](https://github.com/ai4ce/MARS)] [[paper](https://arxiv.org/abs/2406.09383)] [[project](https://ai4ce.github.io/MARS/)]
- {Real} **RCooper** (RCooper: A Real-World Large-Scale Dataset for Roadside Cooperative Perception) [[paper](https://arxiv.org/abs/2403.10145)] [[code](https://github.com/AIR-THU/DAIR-RCooper)] [[project](https://www.t3caic.com/qingzhen)]
- {Real} **TUMTraf-V2X** (TUMTraf V2X Cooperative Perception Dataset) [[paper](https://arxiv.org/abs/2403.01316)] [[code](https://github.com/tum-traffic-dataset/tum-traffic-dataset-dev-kit)] [[project](https://tum-traffic-dataset.github.io/tumtraf-v2x)]

### ECCV 2024

- {Real} **H-V2X** (H-V2X: A Large Scale Highway Dataset for BEV Perception) [[paper](https://eccv2024.ecva.net/virtual/2024/poster/126)] [~~code~~] [~~project~~]

### ICLR 2024

- **OPV2V-H** (An Extensible Framework for Open Heterogeneous Collaborative Perception) [[paper&review](https://openreview.net/forum?id=KkrDUGIASk)] [[code](https://github.com/yifanlu0227/HEAL)] [[project](https://huggingface.co/datasets/yifanlu/OPV2V-H)]

### AAAI 2024

- **DeepAccident** (DeepAccident: A Motion and Accident Prediction Benchmark for V2X Autonomous Driving) [[paper](https://arxiv.org/abs/2304.01168)] [[code](https://github.com/tianqi-wang1996/DeepAccident)] [[project](https://deepaccident.github.io)]

### CVPR 2023

- **CoPerception-UAV+** (Collaboration Helps Camera Overtake LiDAR in 3D Detection) [[paper](https://arxiv.org/abs/2303.13560)] [[code](https://github.com/MediaBrain-SJTU/CoCa3D)] [[project](https://siheng-chen.github.io/dataset/CoPerception+)]
- **OPV2V+** (Collaboration Helps Camera Overtake LiDAR in 3D Detection) [[paper](https://arxiv.org/abs/2303.13560)] [[code](https://github.com/MediaBrain-SJTU/CoCa3D)] [[project](https://siheng-chen.github.io/dataset/CoPerception+)]
- {Real} **V2V4Real** (V2V4Real: A Large-Scale Real-World Dataset for Vehicle-to-Vehicle Cooperative Perception) [[paper](https://arxiv.org/abs/2303.07601)] [[code](https://github.com/ucla-mobility/V2V4Real)] [[project](https://mobility-lab.seas.ucla.edu/v2v4real)]
- {Real} **DAIR-V2X-Seq** (V2X-Seq: The Large-Scale Sequential Dataset for the Vehicle-Infrastructure Cooperative Perception and Forecasting) [[paper](https://arxiv.org/abs/2305.05938)] [[code](https://github.com/AIR-THU/DAIR-V2X-Seq)] [[project](https://thudair.baai.ac.cn/index)]

### NeurIPS 2023

- **IRV2V** (Robust Asynchronous Collaborative 3D Detection via Bird's Eye View Flow) [[paper&review](https://openreview.net/forum?id=UHIDdtxmVS)] [~~code~~] [~~project~~]

### ICCV 2023

- **Roadside-Opt** (Optimizing the Placement of Roadside LiDARs for Autonomous Driving) [[paper](https://arxiv.org/abs/2310.07247)] [~~code~~] [~~project~~]

### ICRA 2023

- {Real} **DAIR-V2X-C Complemented** (Robust Collaborative 3D Object Detection in Presence of Pose Errors) [[paper](https://arxiv.org/abs/2211.07214)] [[code](https://github.com/yifanlu0227/CoAlign)] [[project](https://siheng-chen.github.io/dataset/dair-v2x-c-complemented)]
- **RLS** (Analyzing Infrastructure LiDAR Placement with Realistic LiDAR Simulation Library) [[paper](https://arxiv.org/abs/2211.15975)] [[code](https://github.com/PJLab-ADG/LiDARSimLib-and-Placement-Evaluation)] [~~project~~]
- **V2XP-ASG** (V2XP-ASG: Generating Adversarial Scenes for Vehicle-to-Everything Perception) [[paper](https://arxiv.org/abs/2209.13679)] [[code](https://github.com/XHwind/V2XP-ASG)] [~~project~~]

### CVPR 2022

- **AutoCastSim** (COOPERNAUT: End-to-End Driving with Cooperative Perception for Networked Vehicles) [[paper](https://arxiv.org/abs/2205.02222)] [[code](https://github.com/hangqiu/AutoCastSim)] [[project](https://utexas.app.box.com/v/coopernaut-dataset)]
- {Real} **DAIR-V2X** (DAIR-V2X: A Large-Scale Dataset for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper](https://arxiv.org/abs/2204.05575)] [[code](https://github.com/AIR-THU/DAIR-V2X)] [[project](https://thudair.baai.ac.cn/index)]

### NeurIPS 2022

- **CoPerception-UAV** (Where2comm: Efficient Collaborative Perception via Spatial Confidence Maps) [[paper&review](https://openreview.net/forum?id=dLL4KXzKUpS)] [[code](https://github.com/MediaBrain-SJTU/where2comm)] [[project](https://siheng-chen.github.io/dataset/coperception-uav)]

### ECCV 2022

- **V2XSet** (V2X-ViT: Vehicle-to-Everything Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2203.10638)] [[code](https://github.com/DerrickXuNu/v2x-vit)] [[project](https://drive.google.com/drive/folders/1r5sPiBEvo8Xby-nMaWUTnJIPK6WhY1B6)]

### ICRA 2022

- **OPV2V** (OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication) [[paper](https://arxiv.org/abs/2109.07644)] [[code](https://github.com/DerrickXuNu/OpenCOOD)] [[project](https://mobility-lab.seas.ucla.edu/opv2v)]

### ACCV 2022

- **DOLPHINS** (DOLPHINS: Dataset for Collaborative Perception Enabled Harmonious and Interconnected Self-Driving) [[paper](https://arxiv.org/abs/2207.07609)] [[code](https://github.com/explosion5/Dolphins)] [[project](https://dolphins-dataset.net)]

### ICCV 2021

- **V2X-Sim** (V2X-Sim: Multi-Agent Collaborative Perception Dataset and Benchmark for Autonomous Driving) [[paper](https://arxiv.org/abs/2202.08449)] [[code](https://github.com/ai4ce/V2X-Sim)] [[project](https://ai4ce.github.io/V2X-Sim)]

### CoRL 2017

- **CARLA** (CARLA: An Open Urban Driving Simulator) [[paper](https://arxiv.org/abs/1711.03938)] [[code](https://github.com/carla-simulator/carla)] [[project](https://carla.org)]