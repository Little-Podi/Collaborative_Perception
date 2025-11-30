# Collaborative Perception

This repository is a paper digest of recent advances in **collaborative** / **cooperative** / **multi-agent** perception for **V2I** / **V2V** / **V2X** autonomous driving scenario. Papers are listed in alphabetical order of the first character.

### :link:Jump to:
- ### [[Method and Framework](https://github.com/Little-Podi/Collaborative_Perception#bookmarkmethod-and-framework)]
- ### [[Dataset and Simulator](https://github.com/Little-Podi/Collaborative_Perception#bookmarkdataset-and-simulator)]

Note: I find it hard to fairly compare all methods on each benchmark since some published results are obtained without specified training and testing settings, or even modified model architectures. In fact, many works evaluate all baselines under their own settings and report them. Therefore, it is probably to find inconsistency between papers. Hence, I discard the collection and reproducton of all the benchmarks in a previous update. If you are interested, you can find a bunch of results in [this archived version](https://github.com/Little-Podi/Collaborative_Perception/tree/1be25908aea0a9f635ff4852b3a90729cf2b6aac).



## :star2:Recommendation

### Helpful Learning Resource:thumbsup::thumbsup::thumbsup:

- **(Position)** When Autonomous Vehicle Meets V2X Cooperative Perception: How Far Are We? [[paper](https://arxiv.org/abs/2509.24927)], Research Challenges and Progress in the End-to-End V2X Cooperative Autonomous Driving Competition [[paper](https://arxiv.org/abs/2507.21610)], Automated Vehicles Should be Connected with Natural Language [[paper](https://arxiv.org/abs/2507.01059)], Collaborative Perception Datasets for Autonomous Driving: A Review [[paper](https://arxiv.org/abs/2504.12696)], Collaborative Perception for Connected and Autonomous Driving: Challenges, Possible Solutions and Opportunities [[paper](https://arxiv.org/abs/2401.01544)], V2X Cooperative Perception for Autonomous Driving: Recent Advances and Challenges [[paper](https://arxiv.org/abs/2310.03525)], Towards Vehicle-to-Everything Autonomous Driving: A Survey on Collaborative Perception [[paper](https://arxiv.org/abs/2308.16714)], Collaborative Perception in Autonomous Driving: Methods, Datasets and Challenges [[paper](https://arxiv.org/abs/2301.06262)], A Survey and Framework of Cooperative Perception: From Heterogeneous Singleton to Hierarchical Cooperation [[paper](https://arxiv.org/abs/2208.10590)]
- **(Talk)** Vehicle-to-Vehicle (V2V) Communication (Waabi CVPR 24 Tutorial on Self-Driving Cars) [[video](https://youtu.be/yceuUthWz9s)], Vehicle-to-Vehicle (V2V) Communication (Waabi CVPR 23 Tutorial on Self-Driving Cars) [[video](https://youtu.be/T-N51B8mZB8)], The Ultimate Solution for L4 Autonomous Driving [[video](https://youtu.be/cyNxemm4Ujg)], When Vision Transformers Meet Cooperative Perception [[video](https://youtu.be/rLAU4eqoOIU)], Scene Understanding beyond the Visible [[video](https://youtu.be/oz0AnmJZCR4)], Robust Collaborative Perception against Communication Interruption [[video](https://youtu.be/3cIWpMrsyeE)], Collaborative and Adversarial 3D Perception for Autonomous Driving [[video](https://youtu.be/W-AONQMfGi0)], Vehicle-to-Vehicle Communication for Self-Driving [[video](https://youtu.be/oikdOpmIoc4)], Adversarial Robustness for Self-Driving [[video](https://youtu.be/8uBFXzyII5Y)], L4感知系统的终极形态：协同驾驶 [[video](https://youtu.be/NvixMEDHht4)], CoBEVFlow-解决车-车/路协同感知的时序异步问题 [[video](https://youtu.be/IBTgalAjye8)], 新一代协作感知Where2comm减少通信带宽十万倍 [[video](https://youtu.be/i5coMk4hkuk)], 从任务相关到任务无关的多机器人协同感知 [[video](https://course.zhidx.com/c/MDlkZjcyZDgwZWI4ODBhOGQ4MzM=)], 协同自动驾驶：仿真与感知 [[video](https://course.zhidx.com/c/MmQ1YWUyMzM1M2I3YzVlZjE1NzM=)], 基于群体协作的超视距态势感知 [[video](https://www.koushare.com/video/videodetail/33015)]
- **(Library)** V2Xverse: A Codebase for V2X-Based Collaborative End2End Autonomous Driving [[code](https://github.com/CollaborativePerception/V2Xverse)] [[doc](https://collaborativeperception.github.io/V2Xverse)], HEAL: An Extensible Framework for Open Heterogeneous Collaborative Perception [[code](https://github.com/yifanlu0227/HEAL)] [[doc](https://huggingface.co/yifanlu/HEAL)], OpenCOOD: Open Cooperative Detection Framework for Autonomous Driving [[code](https://github.com/DerrickXuNu/OpenCOOD)] [[doc](https://opencood.readthedocs.io/en/latest/index.html)], CoPerception: SDK for Collaborative Perception [[code](https://github.com/coperception/coperception)] [[doc](https://coperception.readthedocs.io/en/latest)], OpenCDA: Simulation Tool Integrated with Prototype Cooperative Driving Automation [[code](https://github.com/ucla-mobility/OpenCDA)] [[doc](https://opencda-documentation.readthedocs.io/en/latest)]
- **(Workshop)** Co-Intelligence@ECCV'24 [[web](https://coop-intelligence.github.io)], CoPerception@ICRA'23 [[web](https://coperception.github.io)], ScalableAD@ICRA'23 [[web](https://sites.google.com/view/icra2023av/home)]
- **(Background)** Current Approaches and Future Directions for Point Cloud Object Detection in Intelligent Agents [[video](https://youtu.be/xFFCQVwYeec)], 3D Object Detection for Autonomous Driving: A Review and New Outlooks [[paper](https://arxiv.org/abs/2206.09474)], DACOM: Learning Delay-Aware Communication for Multi-Agent Reinforcement Learning [[video](https://youtu.be/YBgW2oA_n3k)], A Survey of Multi-Agent Reinforcement Learning with Communication [[paper](https://arxiv.org/abs/2203.08975)]

### Typical Collaboration Modes:handshake::handshake::handshake:

![](mode.png)

### Possible Optimization Directions:fire::fire::fire:

![](direction.png)



## :bookmark:Method and Framework

Note: {Related} denotes that it is not a pure collaborative perception paper but has related content.

### Selected Preprint

- **ACCO** (Is Discretization Fusion All You Need for Collaborative Perception?) [[paper](https://arxiv.org/abs/2503.13946)] [[code](https://github.com/sidiangongyuan/ACCO)]
- **AR2VP** (Dynamic V2X Autonomous Perception from Road-to-Vehicle Vision) [[paper](https://arxiv.org/abs/2310.19113)] [[code](https://github.com/tjy1423317192/AP2VP)]
- **CPPC** (Point Cluster: A Compact Message Unit for Communication-Efficient Collaborative Perception) [[paper&review](https://openreview.net/forum?id=54XlM8Clkg)] [~~code~~]
- **CP-FREEZER** (CP-FREEZER: Latency Attacks against Vehicular Cooperative Perception) [[paper](https://arxiv.org/abs/2508.01062)] [[code](https://github.com/WiSeR-Lab/CP-FREEZER)]
- **CMP** (CMP: Cooperative Motion Prediction with Multi-Agent Communication) [[paper](https://arxiv.org/abs/2403.17916)] [~~code~~]
- **CoBEVFusion** (CoBEVFusion: Cooperative Perception with LiDAR-Camera Bird's-Eye View Fusion) [[paper](https://arxiv.org/abs/2310.06008)] [~~code~~]
- **CoBEVGlue** (Self-Localized Collaborative Perception) [[paper](https://arxiv.org/abs/2406.12712)] [[code](https://github.com/VincentNi0107/CoBEVGlue)]
- **CoCMT** (CoCMT: Towards Communication-Efficient Corss-Modal Transformer For Collaborative Perception) [[paper&review](https://openreview.net/forum?id=S1NrbfMS7T)] [[code](https://github.com/taco-group/COCMT)]
- **CoDiff** (CoDiff: Conditional Diffusion Model for Collaborative 3D Object Detection) [[paper](https://arxiv.org/abs/2502.14891)] [~~code~~]
- **CoDriving** (Towards Collaborative Autonomous Driving: Simulation Platform and End-to-End System) [[paper](https://arxiv.org/abs/2404.09496)] [[code](https://github.com/CollaborativePerception/V2Xverse)]
- **CoDrivingLLM** (Towards Interactive and Learnable Cooperative Driving Automation: A Large Language Model-Driven Decision-making Framework) [[paper](https://arxiv.org/abs/2409.12812)] [[code](https://github.com/FanGShiYuu/CoDrivingLLM)]
- **CollaMamba** (CollaMamba: Efficient Collaborative Perception with Cross-Agent Spatial-Temporal State Space Model) [[paper](https://arxiv.org/abs/2409.07714)] [~~code~~]
- **CoLMDriver** (CoLMDriver: LLM-Based Negotiation Benefits Cooperative Autonomous Driving) [[paper](https://arxiv.org/abs/2503.08683)] [[code](https://github.com/cxliu0314/CoLMDriver)]
- **CoMamba** (CoMamba: Real-Time Cooperative Perception Unlocked with State Space Models) [[paper](https://arxiv.org/abs/2409.10699)] [~~code~~]
- **CoPLOT** (Beyond BEV: Optimizing Point-Level Tokens for Collaborative Perception) [[paper](https://arxiv.org/abs/2508.19638)] [[code](https://github.com/CheeryLeeyy/CoPLOT)]
- **CP-Guard+** (CP-Guard+: A New Paradigm for Malicious Agent Detection and Defense in Collaborative Perception) [[paper&review](https://openreview.net/forum?id=9MNzHTSDgh)] [~~code~~]
- **CTCE** (Leveraging Temporal Contexts to Enhance Vehicle-Infrastructure Cooperative Perception) [[paper](https://arxiv.org/abs/2408.10531)] [~~code~~]
- **Debrief** (Talking Vehicles: Cooperative Driving via Natural Language) [[paper&review](https://openreview.net/forum?id=VYlfoA8I6A)] [~~code~~]
- **DeepFleet** (DeepFleet: Multi-Agent Foundation Models for Mobile Robots) [[paper](https://arxiv.org/abs/2508.08574)] [~~code~~]
- **DiffCP** (DiffCP: Ultra-Low Bit Collaborative Perception via Diffusion Model) [[paper](https://arxiv.org/abs/2409.19592)] [~~code~~]
- **FadeLead** (Background Fades, Foreground Leads: Curriculum-Guided Background Pruning for Efficient Foreground-Centric Collaborative Perception) [[paper](https://arxiv.org/abs/2510.19250)] [~~code~~]
- **HeatV2X** (HeatV2X: Scalable Heterogeneous Collaborative Perception via Efficient Alignment and Interaction) [[paper](https://arxiv.org/abs/2511.10211)] [[code](https://github.com/hollowknight2167/HeatV2X)]
- **HyComm** (Communication-Efficient Multi-Agent 3D Detection via Hybrid Collaboration) [[paper](https://arxiv.org/abs/2508.07092)] [~~code~~]
- **InSPE** (InSPE: Rapid Evaluation of Heterogeneous Multi-Modal Infrastructure Sensor Placement) [[paper](https://arxiv.org/abs/2504.08240)] [~~code~~]
- **I2XTraj** (Knowledge-Informed Multi-Agent Trajectory Prediction at Signalized Intersections for Infrastructure-to-Everything) [[paper](https://arxiv.org/abs/2501.13461)] [~~code~~]
- **JigsawComm** (JigsawComm: Joint Semantic Feature Encoding and Transmission for Communication-Efficient Cooperative Perception) [[paper](https://arxiv.org/abs/2511.17843)] [[code](https://github.com/WiSeR-Lab/JigsawComm)]
- **LCV2I** (LCV2I: Communication-Efficient and High-Performance Collaborative Perception Framework with Low-Resolution LiDAR) [[paper](https://arxiv.org/abs/2502.17039)] [~~code~~]
- **LMMCoDrive** (LMMCoDrive: Cooperative Driving with Large Multimodal Model) [[paper](https://arxiv.org/abs/2409.11981)] [[code](https://github.com/henryhcliu/LMMCoDrive)]
- {Related} **MDG** (MDG: Masked Denoising Generation for Multi-Agent Behavior Modeling in Traffic Environments) [[paper](https://arxiv.org/abs/2511.17496)] [~~code~~]
- **mmCooper** (mmCooper: A Multi-Agent Multi-Stage Communication-Efficient and Collaboration-Robust Cooperative Perception Framework) [[paper](https://arxiv.org/abs/2501.12263)] [~~code~~]
- **MOT-CUP** (Collaborative Multi-Object Tracking with Conformal Uncertainty Propagation) [[paper](https://arxiv.org/abs/2303.14346)] [[code](https://github.com/susanbao/mot_cup)]
- **RDComm** (Rate-Distortion Optimized Communication for Collaborative Perception) [[paper&review](https://openreview.net/forum?id=920RxFvsMx)] [~~code~~]
- **RefPtsFusion** (From Features to Reference Points: Lightweight and Adaptive Fusion for Cooperative Autonomous Driving) [[paper](https://arxiv.org/abs/2511.18757)] [~~code~~]
- {Related} **RopeBEV** (RopeBEV: A Multi-Camera Roadside Perception Network in Bird's-Eye-View) [[paper](https://arxiv.org/abs/2409.11706)] [~~code~~]
- **ParCon** (ParCon: Noise-Robust Collaborative Perception via Multi-Module Parallel Connection) [[paper](https://arxiv.org/abs/2407.11546)] [~~code~~]
- **PragComm** (Pragmatic Communication in Multi-Agent Collaborative Perception) [[paper](https://arxiv.org/abs/2401.12694)] [[code](https://github.com/PhyllisH/PragComm)]
- **QuantV2X** (QuantV2X: A Fully Quantized Multi-Agent System for Cooperative Perception) [[paper](https://arxiv.org/abs/2509.03704)] [[code](https://github.com/ucla-mobility/QuantV2X)]
- **QUEST** (QUEST: Query Stream for Vehicle-Infrastructure Cooperative Perception) [[paper](https://arxiv.org/abs/2308.01804)] [~~code~~]
- **RCDN** (RCDN: Towards Robust Camera-Insensitivity Collaborative Perception via Dynamic Feature-Based 3D Neural Modeling) [[paper](https://arxiv.org/abs/2405.16868)] [~~code~~]
- **ReVQom** (Residual Vector Quantization For Communication-Efficient Multi-Agent Perception) [[paper](https://arxiv.org/abs/2509.21464)] [~~code~~]
- **RG-Attn** (RG-Attn: Radian Glue Attention for Multi-Modality Multi-Agent Cooperative Perception) [[paper](https://arxiv.org/abs/2501.16803)] [~~code~~]
- **RiskMM** (Risk Map As Middleware: Towards Interpretable Cooperative End-to-End Autonomous Driving for Risk-Aware Planning) [[paper](https://arxiv.org/abs/2508.07686)] [~~code~~]
- **RoCo-Sim** (RoCo-Sim: Enhancing Roadside Collaborative Perception through Foreground Simulation) [[paper](https://arxiv.org/abs/2503.10410)] [[code](https://github.com/duyuwen-duen/RoCo-Sim)]
- **SafeCoop** (SafeCoop: Unravelling Full Stack Safety in Agentic Collaborative Driving) [[paper](https://arxiv.org/abs/2510.18123)] [[code](https://github.com/taco-group/SafeCoop)]
- **SiCP** (SiCP: Simultaneous Individual and Cooperative Perception for 3D Object Detection in Connected and Automated Vehicles) [[paper](https://arxiv.org/abs/2312.04822)] [[code](https://github.com/DarrenQu/SiCP)]
- **SparseAlign** (SparseAlign: A Fully Sparse Framework for Cooperative Object Detection) [[paper](https://arxiv.org/abs/2503.12982)] [~~code~~]
- **Talking Vehicles** (Towards Natural Language Communication for Cooperative Autonomous Driving via Self-Play) [[paper](https://arxiv.org/abs/2505.18334)] [[code](https://github.com/cuijiaxun/talking-vehicles)]
- **TOCOM-V2I** (Task-Oriented Communication for Vehicle-to-Infrastructure Cooperative Perception) [[paper](https://arxiv.org/abs/2407.20748)] [~~code~~]
- {Related} **TYP** (Transfer Your Perspective: Controllable 3D Generation from Any Viewpoint in a Driving Scene) [[paper](https://arxiv.org/abs/2502.06682)] [~~code~~]
- **UniMM-V2X** (UniMM-V2X: MoE-Enhanced Multi-Level Fusion for End-to-End Cooperative Autonomous Driving) [[paper](https://arxiv.org/abs/2511.09013)] [[code](https://github.com/Souig/UniMM-V2X)]
- **VIMI** (VIMI: Vehicle-Infrastructure Multi-View Intermediate Fusion for Camera-Based 3D Object Detection) [[paper](https://arxiv.org/abs/2303.10975)] [[code](https://github.com/Bosszhe/VIMI)]
- **VLIF** (Is Intermediate Fusion All You Need for UAV-Based Collaborative Perception?) [[paper](https://arxiv.org/abs/2504.21774)] [[code](https://github.com/uestchjw/LIF)]
- **V2V-GoT** (V2V-GoT: Vehicle-to-Vehicle Cooperative Autonomous Driving with Multimodal Large Language Models and Graph-of-Thoughts) [[paper](https://arxiv.org/abs/2509.18053)] [~~code~~]
- **V2V-LLM** (V2V-LLM: Vehicle-to-Vehicle Cooperative Autonomous Driving with Multi-Modal Large Language Models) [[paper](https://arxiv.org/abs/2502.09980)] [[code](https://github.com/eddyhkchiu/V2VLLM)]
- **V2XPnP** (V2XPnP: Vehicle-to-Everything Spatio-Temporal Fusion for Multi-Agent Perception and Prediction) [[paper](https://arxiv.org/abs/2412.01812)] [[code](https://github.com/Zewei-Zhou/V2XPnP)]
- **V2X-DGPE** (V2X-DGPE: Addressing Domain Gaps and Pose Errors for Robust Collaborative 3D Object Detection) [[paper](https://arxiv.org/abs/2501.02363)] [[code](https://github.com/wangsch10/V2X-DGPE)]
- **V2X-DGW** (V2X-DGW: Domain Generalization for Multi-Agent Perception under Adverse Weather Conditions) [[paper](https://arxiv.org/abs/2403.11371)] [~~code~~]
- **V2X-M2C** (V2X-M2C: Efficient Multi-Module Collaborative Perception with Two Connections) [[paper](https://arxiv.org/abs/2407.11546)] [~~code~~]
- **V2X-PC** (V2X-PC: Vehicle-to-Everything Collaborative Perception via Point Cluster) [[paper](https://arxiv.org/abs/2403.16635)] [~~code~~]
- **V2X-REALM** (V2X-REALM: Vision-Language Model-Based Robust End-to-End Cooperative Autonomous Driving with Adaptive Long-Tail Modeling) [[paper](https://arxiv.org/abs/2506.21041)] [~~code~~]
- **V2X-RECT** (V2X-RECT: An Efficient V2X Trajectory Prediction Framework via Redundant Interaction Filtering and Tracking Error Correction) [[paper](https://arxiv.org/abs/2511.17941)] [~~code~~]
- **V2X-ReaLO** (V2X-ReaLO: An Open Online Framework and Dataset for Cooperative Perception in Reality) [[paper](https://arxiv.org/abs/2503.10034)] [~~code~~]
- **V2X-UniPool** (V2X-UniPool: Unifying Multimodal Perception and Knowledge Reasoning for Autonomous Driving) [[paper](https://arxiv.org/abs/2506.02580)] [[code](https://github.com/snowwhite1016/V2X-UniPool)]
- **V2X-VLM** (V2X-VLM: End-to-End V2X Cooperative Autonomous Driving Through Large Vision-Language Models) [[paper](https://arxiv.org/abs/2408.09251)] [~~code~~]

### AAAI 2026

- **V2VLoc** (V2VLoc: Robust GNSS-Free Collaborative Perception via LiDAR Localization) [[paper](https://arxiv.org/abs/2511.14247)] [[code](https://github.com/wklin214-glitch/V2VLoc)]

### CVPR 2025

- **CoGMP** (Generative Map Priors for Collaborative BEV Semantic Segmentation) [[paper](https://openaccess.thecvf.com/content/CVPR2025/html/Fu_Generative_Map_Priors_for_Collaborative_BEV_Semantic_Segmentation_CVPR_2025_paper.html)] [~~code~~]
- **CoSDH** (CoSDH: Communication-Efficient Collaborative Perception via Supply-Demand Awareness and Intermediate-Late Hybridization) [[paper](https://arxiv.org/abs/2503.03430)] [[code](https://github.com/Xu2729/CoSDH)]
- **HeCoFuse** (HeCoFuse: Cross-Modal Complementary V2X Cooperative Perception with Heterogeneous Sensors) [[paper](https://arxiv.org/abs/2507.13677)] [[code](https://github.com/ChuhengWei/HeCoFuse)]
- **LangCoop** (LangCoop: Collaborative Driving with Language) [[paper](https://arxiv.org/abs/2504.13406)] [[code](https://github.com/taco-group/LangCoop)]
- **PolyInter** (One is Plenty: A Polymorphic Feature Interpreter for Immutable Heterogeneous Collaborative Perception) [[paper](https://arxiv.org/abs/2411.16799)] [[code](https://github.com/yuchen-xia/PolyInter)]
- **SparseAlign** (SparseAlign: A Fully Sparse Framework for Cooperative Object Detection) [[paper](https://arxiv.org/abs/2503.12982)] [~~code~~]
- **TraF-Align** (TraF-Align: Trajectory-aware Feature Alignment for Asynchronous Multi-agent Perception) [[paper](https://arxiv.org/abs/2503.19391)] [[code](https://github.com/zhyingS/TraF-Align)]
- **V2X-R** (V2X-R: Cooperative LiDAR-4D Radar Fusion for 3D Object Detection with Denoising Diffusion) [[paper](https://arxiv.org/abs/2411.08402)] [[code](https://github.com/ylwhxht/V2X-R)]

### NeurIPS 2025

- **GenComm** (Pragmatic Heterogeneous Collaborative Perception via Generative Communication Mechanism) [[paper](https://arxiv.org/abs/2510.19618)] [[code](https://github.com/jeffreychou777/GenComm)]
- **NegoCollab** (NegoCollab: A Common Representation Negotiation Approach for Heterogeneous Collaborative Perception) [[paper](https://arxiv.org/abs/2510.27647)] [[code](https://github.com/scz023/NegoCollab)]

### ICCV 2025

- **CoopTrack** (CoopTrack: Exploring End-to-End Learning for Efficient Cooperative Sequential Perception) [[paper](https://arxiv.org/abs/2507.19239)] [[code](https://github.com/zhongjiaru/CoopTrack)]
- **CoST** (CoST: Efficient Collaborative Perception From Unified Spatiotemporal Perspective) [[paper](https://arxiv.org/abs/2508.00359)] [[code](https://github.com/tzhhhh123/CoST)]
- **MamV2XCalib** (MamV2XCalib: V2X-Based Target-Less Infrastructure Camera Calibration with State Space Model) [[paper](https://arxiv.org/abs/2507.23595)] [[code](https://github.com/zhuyaoye/MamV2XCalib)]
- **SlimComm** (SlimComm: Doppler-Guided Sparse Queries for Bandwidth-Efficient Cooperative 3-D Perception) [[paper](https://arxiv.org/abs/2508.13007)] [~~code~~]
- **TurboTrain** (TurboTrain: Towards Efficient and Balanced Multi-Task Learning for Multi-Agent Perception and Prediction) [[paper](https://arxiv.org/abs/2508.04682)] [[code](https://github.com/ucla-mobility/TurboTrain)]

### ICLR 2025

- **CPPC** (Point Cluster: A Compact Message Unit for Communication-Efficient Collaborative Perception) [[paper&review](https://openreview.net/forum?id=54XlM8Clkg)] [~~code~~]
- **R&B-POP** (Learning 3D Perception from Others' Predictions) [[paper&review](https://openreview.net/forum?id=Ylk98vWQuQ)] [[code](https://github.com/jinsuyoo/rnb-pop)]
- **STAMP** (STAMP: Scalable Task- And Model-Agnostic Collaborative Perception) [[paper&review](https://openreview.net/forum?id=8NdNniulYE)] [[code](https://github.com/taco-group/STAMP)]
  
### AAAI 2025

- **CP-Guard** (CP-Guard: Malicious Agent Detection and Defense in Collaborative Bird's Eye View Perception) [[paper](https://arxiv.org/abs/2412.12000)] [~~code~~]
- **DSRC** (DSRC: Learning Density-Insensitive and Semantic-Aware Collaborative Representation against Corruptions) [[paper](https://arxiv.org/abs/2412.10739)] [[code](https://github.com/Terry9a/DSRC)]
- **UniV2X** (End-to-End Autonomous Driving through V2X Cooperation) [[paper](https://arxiv.org/abs/2404.00717)] [[code](https://github.com/AIR-THU/UniV2X)]

### MM 2025

- **How2Compress** (How2Compress: Scalable and Efficient Edge Video Analytics via Adaptive Granular Video Compression) [[paper](https://wyhallenwu.github.io/assets/pdf/paper_archive/how2compress.pdf)] [[code](https://github.com/wyhallenwu/how2compress)]
- **Selective Shift** (Selective Shift: Towards Personalized Domain Adaptation in Multi-Agent Collaborative Perception) [~~paper~~] [~~code~~]

### ICRA 2025

- **CoDynTrust** (CoDynTrust: Robust Asynchronous Collaborative Perception via Dynamic Feature Trust Modulus) [[paper](https://arxiv.org/abs/2502.08169)] [[code](https://github.com/CrazyShout/CoDynTrust)]
- **CoopDETR** (CoopDETR: A Unified Cooperative Perception Framework for 3D Detection via Object Query) [[paper](https://arxiv.org/abs/2502.19313)] [~~code~~]
- **Co-MTP** (Co-MTP: A Cooperative Trajectory Prediction Framework with Multi-Temporal Fusion for Autonomous Driving) [[paper](https://arxiv.org/abs/2502.16589)] [[code](https://github.com/xiaomiaozhang/Co-MTP)]
- **Direct-CP** (Direct-CP: Directed Collaborative Perception for Connected and Autonomous Vehicles via Proactive Attention) [[paper](https://arxiv.org/abs/2409.08840)] [~~code~~]
- **V2X-DG** (V2X-DG: Domain Generalization for Vehicle-to-Everything Cooperative Perception) [[paper](https://arxiv.org/abs/2503.15435)] [~~code~~]

### IROS 2025

- **CooPre** (CooPre: Cooperative Pretraining for V2X Cooperative Perception) [[paper](https://arxiv.org/abs/2408.11241)] [[code](https://github.com/ucla-mobility/CooPre)]
- **CoPAD** (CoPAD : Multi-source Trajectory Fusion and Cooperative Trajectory Prediction with Anchor-Oriented Decoder in V2X Scenarios) [[paper](https://arxiv.org/abs/2509.15984)] [~~code~~]
- **CRUISE** (CRUISE: Cooperative Reconstruction and Editing in V2X Scenarios using Gaussian Splatting) [[paper](https://arxiv.org/abs/2507.18473)] [[code](https://github.com/SainingZhang/CRUISE)]

### CVPR 2024

- **CoHFF** (Collaborative Semantic Occupancy Prediction with Hybrid Feature Fusion in Connected Automated Vehicles) [[paper](https://arxiv.org/abs/2402.07635)] [~~code~~]
- **CoopDet3D** (TUMTraf V2X Cooperative Perception Dataset) [[paper](https://arxiv.org/abs/2403.01316)] [[code](https://github.com/tum-traffic-dataset/coopdet3d)]
- **CodeFilling** (Communication-Efficient Collaborative Perception via Information Filling with Codebook) [[paper](https://arxiv.org/abs/2405.04966)] [[code](https://github.com/PhyllisH/CodeFilling)]
- **ERMVP** (ERMVP: Communication-Efficient and Collaboration-Robust Multi-Vehicle Perception in Challenging Environments) [[paper](https://openaccess.thecvf.com/content/CVPR2024/html/Zhang_ERMVP_Communication-Efficient_and_Collaboration-Robust_Multi-Vehicle_Perception_in_Challenging_Environments_CVPR_2024_paper.html)] [[code](https://github.com/Terry9a/ERMVP)]
- **MRCNet** (Multi-Agent Collaborative Perception via Motion-Aware Robust Communication Network) [[paper](https://openaccess.thecvf.com/content/CVPR2024/html/Hong_Multi-agent_Collaborative_Perception_via_Motion-aware_Robust_Communication_Network_CVPR_2024_paper.html)] [[code](https://github.com/IndigoChildren/collaborative-perception-MRCNet)]

### NeurIPS 2024

- **V2X-Graph** (Learning Cooperative Trajectory Representations for Motion Forecasting) [[paper](https://arxiv.org/abs/2311.00371)] [[code](https://github.com/AIR-THU/V2X-Graph)]

### ECCV 2024

- **Hetecooper** (Hetecooper: Feature Collaboration Graph for Heterogeneous Collaborative Perception) [[paper](https://eccv.ecva.net/virtual/2024/poster/2467)] [~~code~~]
- **Infra-Centric CP** (Rethinking the Role of Infrastructure in Collaborative Perception) [[paper](https://arxiv.org/abs/2410.11259)] [~~code~~]

### ICLR 2024

- **HEAL** (An Extensible Framework for Open Heterogeneous Collaborative Perception) [[paper&review](https://openreview.net/forum?id=KkrDUGIASk)] [[code](https://github.com/yifanlu0227/HEAL)]

### AAAI 2024

- **CMiMC** (What Makes Good Collaborative Views? Contrastive Mutual Information Maximization for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2403.10068)] [[code](https://github.com/77SWF/CMiMC)]
- **DI-V2X** (DI-V2X: Learning Domain-Invariant Representation for Vehicle-Infrastructure Collaborative 3D Object Detection) [[paper](https://arxiv.org/abs/2312.15742)] [[code](https://github.com/Serenos/DI-V2X)]
- **V2XFormer** (DeepAccident: A Motion and Accident Prediction Benchmark for V2X Autonomous Driving) [[paper](https://arxiv.org/abs/2304.01168)] [[code](https://github.com/tianqi-wang1996/DeepAccident)]

### WACV 2024

- **MACP** (MACP: Efficient Model Adaptation for Cooperative Perception) [[paper](https://arxiv.org/abs/2310.16870)] [[code](https://github.com/PurdueDigitalTwin/MACP)]

### ICRA 2024

- **DMSTrack** (Probabilistic 3D Multi-Object Cooperative Tracking for Autonomous Driving via Differentiable Multi-Sensor Kalman Filter) [[paper](https://arxiv.org/abs/2309.14655)] [[code](https://github.com/eddyhkchiu/DMSTrack)]
- **FreeAlign** (Robust Collaborative Perception without External Localization and Clock Devices) [[paper](https://arxiv.org/abs/2405.02965)] [[code](https://github.com/MediaBrain-SJTU/FreeAlign)]

### CVPR 2023

- {Related} **BEVHeight** (BEVHeight: A Robust Framework for Vision-Based Roadside 3D Object Detection) [[paper](https://arxiv.org/abs/2303.08498)] [[code](https://github.com/ADLab-AutoDrive/BEVHeight)]
- **CoCa3D** (Collaboration Helps Camera Overtake LiDAR in 3D Detection) [[paper](https://arxiv.org/abs/2303.13560)] [[code](https://github.com/MediaBrain-SJTU/CoCa3D)]
- **FF-Tracking** (V2X-Seq: The Large-Scale Sequential Dataset for the Vehicle-Infrastructure Cooperative Perception and Forecasting) [[paper](https://arxiv.org/abs/2305.05938)] [[code](https://github.com/AIR-THU/DAIR-V2X-Seq)]

### NeurIPS 2023

- **CoBEVFlow** (Robust Asynchronous Collaborative 3D Detection via Bird's Eye View Flow) [[paper&review](https://openreview.net/forum?id=UHIDdtxmVS)] [[code](https://github.com/MediaBrain-SJTU/CoBEVFlow)]
- **FFNet** (Flow-Based Feature Fusion for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper&review](https://openreview.net/forum?id=gsglrhvQxX)] [[code](https://github.com/haibao-yu/FFNet-VIC3D)]
- **How2comm** (How2comm: Communication-Efficient and Collaboration-Pragmatic Multi-Agent Perception) [[paper&review](https://openreview.net/forum?id=Dbaxm9ujq6)] [[code](https://github.com/ydk122024/How2comm)]

### ICCV 2023

- **CORE** (CORE: Cooperative Reconstruction for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2307.11514)] [[code](https://github.com/zllxot/CORE)]
- **HM-ViT** (HM-ViT: Hetero-Modal Vehicle-to-Vehicle Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2304.10628)] [[code](https://github.com/XHwind/HM-ViT)]
- **ROBOSAC** (Among Us: Adversarially Robust Collaborative Perception by Consensus) [[paper](https://arxiv.org/abs/2303.09495)] [[code](https://github.com/coperception/ROBOSAC)]
- **SCOPE** (Spatio-Temporal Domain Awareness for Multi-Agent Collaborative Perception) [[paper](https://arxiv.org/abs/2307.13929)] [[code](https://github.com/starfdu1418/SCOPE)]
- **TransIFF** (TransIFF: An Instance-Level Feature Fusion Framework for Vehicle-Infrastructure Cooperative 3D Detection with Transformers) [[paper](https://openaccess.thecvf.com/content/ICCV2023/html/Chen_TransIFF_An_Instance-Level_Feature_Fusion_Framework_for_Vehicle-Infrastructure_Cooperative_3D_ICCV_2023_paper.html)] [~~code~~]
- **UMC** (UMC: A Unified Bandwidth-Efficient and Multi-Resolution Based Collaborative Perception Framework) [[paper](https://arxiv.org/abs/2303.12400)] [[code](https://github.com/ispc-lab/UMC)]

### ICLR 2023

- {Related} **CO3** (CO3: Cooperative Unsupervised 3D Representation Learning for Autonomous Driving) [[paper&review](https://openreview.net/forum?id=QUaDoIdgo0)] [[code](https://github.com/Runjian-Chen/CO3)]

### CoRL 2023

- **BM2CP** {BM2CP: Efficient Collaborative Perception with LiDAR-Camera Modalities} [[paper&review](https://openreview.net/forum?id=uJqxFjF1xWp)] [[code](https://github.com/byzhaoAI/BM2CP)]

### MM 2023

- **DUSA** (DUSA: Decoupled Unsupervised Sim2Real Adaptation for Vehicle-to-Everything Collaborative Perception) [[paper](https://arxiv.org/abs/2310.08117)] [[code](https://github.com/refkxh/DUSA)]
- **FeaCo** (FeaCo: Reaching Robust Feature-Level Consensus in Noisy Pose Conditions) [[paper](https://dl.acm.org/doi/abs/10.1145/3581783.3611880)] [[code](https://github.com/jmgu0212/FeaCo)]
- **What2comm** (What2comm: Towards Communication-Efficient Collaborative Perception via Feature Decoupling) [[paper](https://dl.acm.org/doi/abs/10.1145/3581783.3611699)] [~~code~~]

### WACV 2023

- **AdaFusion** (Adaptive Feature Fusion for Cooperative Perception Using LiDAR Point Clouds) [[paper](https://arxiv.org/abs/2208.00116)] [[code](https://github.com/DonghaoQiao/Adaptive-Feature-Fusion-for-Cooperative-Perception)]

### ICRA 2023

- **CoAlign** (Robust Collaborative 3D Object Detection in Presence of Pose Errors) [[paper](https://arxiv.org/abs/2211.07214)] [[code](https://github.com/yifanlu0227/CoAlign)]
- {Related} **DMGM** (Deep Masked Graph Matching for Correspondence Identification in Collaborative Perception) [[paper](https://arxiv.org/abs/2303.07555)] [[code](https://github.com/gaopeng5/DMGM)]
- **Double-M Quantification** (Uncertainty Quantification of Collaborative Detection for Self-Driving) [[paper](https://arxiv.org/abs/2209.08162)] [[code](https://github.com/coperception/double-m-quantification)]
- **MAMP** (Model-Agnostic Multi-Agent Perception Framework) [[paper](https://arxiv.org/abs/2203.13168)] [[code](https://github.com/DerrickXuNu/model_anostic)]
- **MATE** (Communication-Critical Planning via Multi-Agent Trajectory Exchange) [[paper](https://arxiv.org/abs/2303.06080)] [~~code~~]
- **MPDA** (Bridging the Domain Gap for Multi-Agent Perception) [[paper](https://arxiv.org/abs/2210.08451)] [[code](https://github.com/DerrickXuNu/MPDA)]
- **WNT** (We Need to Talk: Identifying and Overcoming Communication-Critical Scenarios for Self-Driving) [[paper](https://arxiv.org/abs/2305.04352)] [~~code~~]

### CVPR 2022

- **Coopernaut** (COOPERNAUT: End-to-End Driving with Cooperative Perception for Networked Vehicles) [[paper](https://arxiv.org/abs/2205.02222)] [[code](https://github.com/UT-Austin-RPL/Coopernaut)]
- {Related} **LAV** (Learning from All Vehicles) [[paper](https://arxiv.org/abs/2203.11934)] [[code](https://github.com/dotchen/LAV)]
- **TCLF** (DAIR-V2X: A Large-Scale Dataset for Vehicle-Infrastructure Cooperative 3D Object Detection) [[paper](https://arxiv.org/abs/2204.05575)] [[code](https://github.com/AIR-THU/DAIR-V2X)]

### NeurIPS 2022

- **Where2comm** (Where2comm: Efficient Collaborative Perception via Spatial Confidence Maps) [[paper&review](https://openreview.net/forum?id=dLL4KXzKUpS)] [[code](https://github.com/MediaBrain-SJTU/where2comm)]

### ECCV 2022

- **SyncNet** (Latency-Aware Collaborative Perception) [[paper](https://arxiv.org/abs/2207.08560)] [[code](https://github.com/MediaBrain-SJTU/SyncNet)]
- **V2X-ViT** (V2X-ViT: Vehicle-to-Everything Cooperative Perception with Vision Transformer) [[paper](https://arxiv.org/abs/2203.10638)] [[code](https://github.com/DerrickXuNu/v2x-vit)]

### CoRL 2022

- **CoBEVT** (CoBEVT: Cooperative Bird's Eye View Semantic Segmentation with Sparse Transformers) [[paper&review](https://openreview.net/forum?id=PAFEQQtDf8s)] [[code](https://github.com/DerrickXuNu/CoBEVT)]
- **STAR** (Multi-Robot Scene Completion: Towards Task-Agnostic Collaborative Perception) [[paper&review](https://openreview.net/forum?id=hW0tcXOJas2)] [[code](https://github.com/coperception/star)]

### IJCAI 2022

- **IA-RCP** (Robust Collaborative Perception against Communication Interruption) [[paper](https://learn-to-race.org/workshop-ai4ad-ijcai2022/papers.html)] [~~code~~]

### MM 2022

- **CRCNet** (Complementarity-Enhanced and Redundancy-Minimized Collaboration Network for Multi-agent Perception) [[paper](https://dl.acm.org/doi/abs/10.1145/3503161.3548197)] [~~code~~]

### ICRA 2022

- **AttFuse** (OPV2V: An Open Benchmark Dataset and Fusion Pipeline for Perception with Vehicle-to-Vehicle Communication) [[paper](https://arxiv.org/abs/2109.07644)] [[code](https://github.com/DerrickXuNu/OpenCOOD)]
- **MP-Pose** (Multi-Robot Collaborative Perception with Graph Neural Networks) [[paper](https://arxiv.org/abs/2201.01760)] [~~code~~]

### NeurIPS 2021

- **DiscoNet** (Learning Distilled Collaboration Graph for Multi-Agent Perception) [[paper&review](https://openreview.net/forum?id=ZRcjSOmYraB)] [[code](https://github.com/ai4ce/DiscoNet)]

### ICCV 2021

- **Adversarial V2V** (Adversarial Attacks On Multi-Agent Communication) [[paper](https://arxiv.org/abs/2101.06560)] [~~code~~]

### IROS 2021

- **MASH** (Overcoming Obstructions via Bandwidth-Limited Multi-Agent Spatial Handshaking) [[paper](https://arxiv.org/abs/2107.00771)] [[code](https://github.com/yifanlu0227/CoAlign)]

### CVPR 2020

- **When2com** (When2com: Multi-Agent Perception via Communication Graph Grouping) [[paper](https://arxiv.org/abs/2006.00176)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]

### ECCV 2020

- **DSDNet** (DSDNet: Deep Structured Self-Driving Network) [[paper](https://arxiv.org/abs/2008.06041)] [~~code~~]
- **V2VNet** (V2VNet: Vehicle-to-Vehicle Communication for Joint Perception and Prediction) [[paper](https://arxiv.org/abs/2008.07519)] [[code](https://github.com/DerrickXuNu/OpenCOOD)]

### CoRL 2020

- **Robust V2V** (Learning to Communicate and Correct Pose Errors) [[paper](https://arxiv.org/abs/2011.05289)] [[code](https://github.com/yifanlu0227/CoAlign)]

### ICRA 2020

- **Who2com** (Who2com: Collaborative Perception via Learnable Handshake Communication) [[paper](https://arxiv.org/abs/2003.09575)] [[code](https://github.com/GT-RIPL/MultiAgentPerception)]
- **MAIN** (Enhancing Multi-Robot Perception via Learned Data Association) [[paper](https://arxiv.org/abs/2107.00769)] [~~code~~]



## :bookmark:Dataset and Simulator

Note: {Real} denotes that the sensor data is obtained by real-world collection instead of simulation.

### Selected Preprint

- **Adver-City** (Adver-City: Open-Source Multi-Modal Dataset for Collaborative Perception Under Adverse Weather Conditions) [[paper](https://arxiv.org/abs/2410.06380)] [[code](https://github.com/QUARRG/Adver-City)] [[project](https://labs.cs.queensu.ca/quarrg/datasets/adver-city)]
- **AirV2X** (AirV2X: Unified Air-Ground Vehicle-to-Everything Collaboration) [[paper](https://arxiv.org/abs/2506.19283)] [[code](https://github.com/taco-group/AirV2X-Perception)] [[project](https://huggingface.co/datasets/xiangbog/AirV2X-Perception)]
- **CATS-V2V** (CATS-V2V: A Real-World Vehicle-to-Vehicle Cooperative Perception Dataset with Complex Adverse Traffic Scenarios) [[paper](https://arxiv.org/abs/2511.11168)] [~~code~~] [[project](https://cats-v2v-dataset.github.io)]
- {Real} **CoInfra** (CoInfra: A Large-Scale Cooperative Infrastructure Perception System and Dataset in Adverse Weather) [[paper](https://arxiv.org/abs/2507.02245)] [[code](https://github.com/NingMingHao/CoInfra)] [~~project~~]
- **CP-GuardBench** (CP-Guard+: A New Paradigm for Malicious Agent Detection and Defense in Collaborative Perception) [[paper&review](https://openreview.net/forum?id=9MNzHTSDgh)] [~~code~~] [~~project~~]
- **Griffin** (Griffin: Aerial-Ground Cooperative Detection and Tracking Dataset and Benchmark) [[paper](https://arxiv.org/abs/2503.06983)] [[code](https://github.com/wang-jh18-SVM/Griffin)] [[project](https://pan.baidu.com/s/1NDgsuHB-QPRiROV73NRU5g)]
- {Real} **InScope** (InScope: A New Real-world 3D Infrastructure-side Collaborative Perception Dataset for Open Traffic Scenarios) [[paper](https://arxiv.org/abs/2407.21581)] [[code](https://github.com/xf-zh/InScope)] [~~project~~]
- {Real} **Mixed Signals** (Mixed Signals: A Diverse Point Cloud Dataset for Heterogeneous LiDAR V2X Collaboration) [[paper](https://arxiv.org/abs/2502.14156)] [[code](https://github.com/chinitaberrio/Mixed-Signals)] [[project](https://mixedsignalsdataset.cs.cornell.edu)]
- **MobileVerse** (MobiVerse: Scaling Urban Mobility Simulation with Hybrid Lightweight Domain-Specific Generator and Large Language Models) [[paper](https://arxiv.org/abs/2506.21784)] [[code](https://github.com/ucla-mobility/MobiVerse)] [~~project~~]
- **Multi-V2X** (Multi-V2X: A Large Scale Multi-modal Multi-penetration-rate Dataset for Cooperative Perception) [[paper](https://arxiv.org/abs/2409.04980)] [[code](https://github.com/RadetzkyLi/Multi-V2X)] [~~project~~]
- **M3CAD** (M3CAD: Towards Generic Cooperative Autonomous Driving Benchmark) [[paper](https://arxiv.org/abs/2505.06746)] [[code](https://github.com/zhumorui/M3CAD)] [[project](https://zhumorui.github.io/m3cad)]
- **OPV2V-N** (RCDN: Towards Robust Camera-Insensitivity Collaborative Perception via Dynamic Feature-Based 3D Neural Modeling) [[paper](https://arxiv.org/abs/2405.16868)] [~~code~~] [~~project~~]
- **TalkingVehiclesGym** (Towards Natural Language Communication for Cooperative Autonomous Driving via Self-Play) [[paper](https://arxiv.org/abs/2505.18334)] [[code](https://github.com/cuijiaxun/talking-vehicles)] [[project](https://talking-vehicles.github.io)]
- **TruckV2X** (TruckV2X: A Truck-Centered Perception Dataset) [[paper](https://arxiv.org/abs/2507.09505)] [~~code~~] [[project](https://xietenghu1.github.io/TruckV2X)]
- **V2V-QA** (V2V-LLM: Vehicle-to-Vehicle Cooperative Autonomous Driving with Multi-Modal Large Language Models) [[paper](https://arxiv.org/abs/2502.09980)] [[code](https://github.com/eddyhkchiu/V2VLLM)] [[project](https://eddyhkchiu.github.io/v2vllm.github.io)]
- {Real} **V2XPnP-Seq** (V2XPnP: Vehicle-to-Everything Spatio-Temporal Fusion for Multi-Agent Perception and Prediction) [[paper](https://arxiv.org/abs/2412.01812)] [[code](https://github.com/Zewei-Zhou/V2XPnP)] [[project](https://mobility-lab.seas.ucla.edu/v2xpnp)]
- {Real} **V2X-Radar** (V2X-Radar: A Multi-Modal Dataset with 4D Radar for Cooperative Perception) [[paper](https://arxiv.org/abs/2411.10962)] [[code](https://github.com/yanglei18/V2X-Radar)] [[project](http://openmpd.com/column/V2X-Radar)]
- {Real} **V2X-Real** (V2X-Real: a Large-Scale Dataset for Vehicle-to-Everything Cooperative Perception) [[paper](https://arxiv.org/abs/2403.16034)] [~~code~~] [[project](https://mobility-lab.seas.ucla.edu/v2x-real)]
- {Real} **V2X-ReaLO** (V2X-ReaLO: An Open Online Framework and Dataset for Cooperative Perception in Reality) [[paper](https://arxiv.org/abs/2503.10034)] [~~code~~] [~~project~~]
- **WHALES** (WHALES: A Multi-Agent Scheduling Dataset for Enhanced Cooperation in Autonomous Driving) [[paper](https://arxiv.org/abs/2411.13340)] [[code](https://github.com/chensiweiTHU/WHALES)] [[project](https://pan.baidu.com/s/1dintX-d1T-m2uACqDlAM9A)]

### CVPR 2025

- **Mono3DVLT-V2X** (Mono3DVLT: Monocular-Video-Based 3D Visual Language Tracking) [[paper](https://openaccess.thecvf.com/content/CVPR2025/html/Wei_Mono3DVLT_Monocular-Video-Based_3D_Visual_Language_Tracking_CVPR_2025_paper.html)] [~~code~~] [~~project~~]
- **RCP-Bench** (RCP-Bench: Benchmarking Robustness for Collaborative Perception Under Diverse Corruptions) [[paper](https://openaccess.thecvf.com/content/CVPR2025/html/Du_RCP-Bench_Benchmarking_Robustness_for_Collaborative_Perception_Under_Diverse_Corruptions_CVPR_2025_paper.html)] [[code](https://github.com/LuckyDush/RCP-Bench)] [~~project~~]
- **V2X-R** (V2X-R: Cooperative LiDAR-4D Radar Fusion for 3D Object Detection with Denoising Diffusion) [[paper](https://arxiv.org/abs/2411.08402)] [[code](https://github.com/ylwhxht/V2X-R)] [~~project~~]

### NeurIPS 2025

- {Real} **AGC-Drive** (AGC-Drive: A Large-Scale Dataset for Real-World Aerial-Ground Collaboration in Driving Scenarios) [[paper&review](https://openreview.net/forum?id=N07WGSPh9l)] [[code](https://github.com/PercepX/AGC-Drive)] [[project](https://agc-drive.github.io)]
- **UrbanIng-V2X** (UrbanIng-V2X: A Large-Scale Multi-Vehicle, Multi-Infrastructure Dataset Across Multiple Intersections for Cooperative Perception) [[paper&review](https://openreview.net/forum?id=iSwIkUqyqf)] [[code](https://github.com/thi-ad/UrbanIng-V2X)] [[project](https://pypi.org/project/urbaning)]

### CVPR 2024

- {Real} **HoloVIC** (HoloVIC: Large-Scale Dataset and Benchmark for Multi-Sensor Holographic Intersection and Vehicle-Infrastructure Cooperative) [[paper](https://arxiv.org/abs/2403.02640)] [~~code~~] [[project](https://holovic.net)]
- {Real} **Open Mars Dataset** (Multiagent Multitraversal Multimodal Self-Driving: Open MARS Dataset) [[code](https://github.com/ai4ce/MARS)] [[paper](https://arxiv.org/abs/2406.09383)] [[project](https://ai4ce.github.io/MARS)]
- {Real} **RCooper** (RCooper: A Real-World Large-Scale Dataset for Roadside Cooperative Perception) [[paper](https://arxiv.org/abs/2403.10145)] [[code](https://github.com/AIR-THU/DAIR-RCooper)] [[project](https://www.t3caic.com/qingzhen)]
- {Real} **TUMTraf-V2X** (TUMTraf V2X Cooperative Perception Dataset) [[paper](https://arxiv.org/abs/2403.01316)] [[code](https://github.com/tum-traffic-dataset/tum-traffic-dataset-dev-kit)] [[project](https://tum-traffic-dataset.github.io/tumtraf-v2x)]

### NeurIPS 2024

- {Real} **DAIR-V2X-Traj** (Learning Cooperative Trajectory Representations for Motion Forecasting) [[paper](https://arxiv.org/abs/2311.00371)] [[code](https://github.com/AIR-THU/V2X-Graph)] [[project](https://thudair.baai.ac.cn/index)]

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
