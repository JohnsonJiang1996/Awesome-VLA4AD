# Awesome Vision–Language–Action Models for Autonomous Driving 🚗
[![arXiv](https://img.shields.io/badge/arXiv-2506.24044-B31B1B.svg?style=flat&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.24044) [![GitHub stars](https://img.shields.io/github/stars/JohnsonJiang1996/Awesome-VLA4AD?style=social)](https://github.com/JohnsonJiang1996/Awesome-VLA4AD/stargazers) [![GitHub forks](https://img.shields.io/github/forks/JohnsonJiang1996/Awesome-VLA4AD?style=social)](https://github.com/JohnsonJiang1996/Awesome-VLA4AD/network)


Welcome to **Awesome VLA4AD**—a curated, continuously updated collection of research papers and resources on Vision–Language–Action models for Autonomous Driving (VLA4AD). This repository tracks the latest advances in VLA4AD, from explanatory perception modules to end-to-end reasoning and control architectures.

Our latest survey is out [here](https://arxiv.org/abs/2506.24044)! We invite your feedback and discussion.

⭐️ **Follow & Star** to stay up to date!  
🤝 **Contributions welcome**—if you know of new papers, datasets, or tools, please open an issue or submit a PR.  
📬 **Questions or suggestions?** Reach us at **sicong.jiang@mail.mcgill.ca** or **qka23@mails.tsinghua.edu.cn**.

---

## 📚 Table of Contents
- [🔥 Motivation & Paradigm Shift](#-overview-of-vla4ad)  
- [🚀 Overview of VLA4AD](#-overview-of-vla4ad)  
- [🏆 Awesome VLA4AD Papers](#-awesome-vla4ad-papers)  
  - [1️⃣ Pre-VLA: VLM as Explainers](#1-pre-vla-vlm-as-explainers)  
  - [2️⃣ Modular VLA4AD](#2-modular-vla4ad)  
  - [3️⃣ End-to-End VLA4AD](#3-end-to-end-vla4ad)  
  - [4️⃣ Reasoning-Augmented VLA4AD](#4-reasoning-augmented-vla4ad)  
- [📊 Datasets & Benchmarks](#-datasets--benchmarks)  
- [⚙️ Installation & Usage](#️-installation--usage)  
- [🤝 Contributing](#-contributing)  
- [⚖️ License](#️-license)  
- [📜 Citation](#-citation)

---
## 🔥 Motivation & Paradigm Shift

The development of autonomous driving has progressed from modular pipelines to fully integrated systems. This survey summarizes the latest advances into three core paradigms:

* **End-to-End AD:** Direct sensor-to-control mapping—efficient but opaque and weak on rare scenarios.  
  * **Flow:** Sensors → Network → Actions

* **VLMs for AD:** Adds language reasoning—boosts explainability but doesn’t drive the vehicle.  
  * **Flow:** Sensors → VLM → Answers

* **VLA for AD:** Unifies vision, language, and control in one policy—understands instructions, reasons, acts, and explains.  
  * **Flow:** Sensors → Multimodal Encoder → LLM/VLM → Decoder → Actions

![Driving Paradigms Comparison](./figs/Paradigm_Comparison.png)  
*Figure 1. (a) conventional end-to-end AD, (b) vision-language models as explainers, (c) full Vision–Language–Action systems.*

---

## 🚀 Overview of VLA4AD

A typical VLA4AD model follows an “Input–Process–Output” flow, unifying environment perception, instruction understanding, and vehicle control.

![Overview of VLA4AD](./figs/Overview_VLA4AD_New.png)  
*Figure 2. Overview of VLA4AD, integrating vision, language, and action modules.*  

A snapshot of the field’s evolution through four successive stages—from VLM-as-explainer to augmented, reasoning-centric agents:

![Progress of VLA Models for AD](./figs/Progress_VLA4AD.png)  
*Figure 3. Progression of VLA4AD models: (1) VLMs as passive explainers; (2) Modular VLA with intermediate representations; (3) End-to-end VLA mapping sensors directly to actions; (4) Augmented VLA with long-horizon reasoning and tool use.*

---


## 🏆 Awesome VLA4AD Papers

### 1️⃣ Pre-VLA: VLM as Explainers
| Model          | Year | Key Features                   | Link                                                             |
| -------------- | ---- | ---------------------- | ---------------------------------------------------------------- |
| DriveGPT-4     | 2023 | Scene Narration, QA    | https://arxiv.org/abs/2310.01412 / [Code](https://tonyxuqaq.github.io/projects/DriveGPT4/)|
| TS-VLM         | 2025 | Text-guided Attention  | https://arxiv.org/abs/2505.12670 / [Code](https://github.com/AiX-Lab-UWO/TS-VLM)|
| DynRsl-VLM     | 2025 | Adaptive Resolution    | https://arxiv.org/abs/2503.11265                                  |

### 2️⃣ Modular VLA4AD
| Model          | Year |  Key Features                      | Link                                                             |
| -------------- | ---- | ---------------------- | ---------------------------------------------------------------- |
| RAG-Driver     | 2024 | Retrieval-Augmented   |https://arxiv.org/abs/2402.10828 / [Code](https://github.com/YuanJianhao508/RAG-Driver)|
| OpenDriveVLA   | 2025 | Language-guided Planning | https://arxiv.org/abs/2503.23463 / [Code](https://github.com/DriveVLA/OpenDriveVLA) |
| DriveMoE       | 2025 | Expert Routing         | https://arxiv.org/abs/2505.16278 / [Code](https://github.com/Thinklab-SJTU/DriveMoE) |
| LangCoop       | 2025 | V2V Coordination       | https://arxiv.org/abs/2504.13406 / [Code](https://github.com/taco-group/LangCoop)  |
| SafeAuto       | 2025 | Rule-based Safety      | https://arxiv.org/abs/2503.00211 / [Code](https://github.com/AI-secure/SafeAuto)  |
| ReCogDrive     | 2025 | Diffusion + RL      |https://arxiv.org/abs/2506.08052 / [Code](https://github.com/xiaomi-research/recogdrive/)  |

### 3️⃣ End-to-End VLA4AD
| Model          | Year |  Key Features                      | Link                                                             |
| -------------- | ---- | ---------------------- | ---------------------------------------------------------------- |
| ADriver-I      | 2023 | Diffusion-based World Model | https://arxiv.org/abs/2311.13549                                  |
| EMMA           | 2024 | Detection + Planning   | https://arxiv.org/abs/2403.04593 / [Code](https://github.com/taco-group/OpenEMMA)  |
| CoVLA-Agent    | 2024 | Caption + Trajectory   | https://arxiv.org/abs/2408.10845 / [Code](https://turingmotors.github.io/covla-ad/)     |
| SimLingo       | 2025 | Action Dreaming        | https://arxiv.org/abs/2503.09594 / [Code](https://github.com/RenzKa/simlingo) |
| DiffVLA        | 2025 | Sparse-Dense Diffusion | https://arxiv.org/abs/2505.19381                                 |

### 4️⃣ Reasoning-Augmented VLA4AD
| Model          | Year |  Key Features                     | Link                                                             |
| -------------- | ---- | ---------------------- | ---------------------------------------------------------------- |
| ORION          | 2025 | Memory + Rationales    | https://arxiv.org/abs/2503.19755 / [Code](https://xiaomi-mlab.github.io/Orion/)              |
| Impromptu-VLA  | 2025 | CoT-Aligned Planning   | https://arxiv.org/abs/2505.23757 / [Code](https://github.com/ahydchh/Impromptu-VLA)           |
| AutoVLA        | 2025 | Drive Tokens + CoT     | https://arxiv.org/abs/2506.13757 / [Code](https://github.com/ucla-mobility/AutoVLA)           |

---

## 📊 Datasets & Benchmarks

| Name                   | Year | Modality                   | Task                      | URL                                       |
| ---------------------- | ---- | -------------------------- | ------------------------- | ----------------------------------------- |
| BDD100K / BDD-X        | 2018 | Video + Rationales         | Captioning, QA            | https://bdd-data.berkeley.edu/            |
| nuScenes               | 2020 | Camera, LiDAR, Radar       | Detection, QA             | https://www.nuscenes.org/                 |
| Bench2Drive            | 2024 | CARLA Simulator            | Closed-loop Driving       | [Github](https://github.com/Thinklab-SJTU/Bench2Drive) |
| Reason2Drive           | 2024 | Video–QA                   | CoT-Chain Consistency     | [Github](https://github.com/fudan-zvg/Reason2Drive)        |
| Impromptu-VLA Dataset  | 2025 | Video + QA + Traj          | Corner-Case Testing       |[Github](https://github.com/ahydchh/Impromptu-VLA)|
| NuInteract              | 2025 | Multi-view QA              | 3D QA                     |[Github](https://github.com/zc-zhao/DriveMonkey)|
| DriveAction            | 2025 | In-the-wild QA             | High-level Actions        |       [HuggingFace](https://huggingface.co/datasets/LiAuto-DriveAction/drive-action)          |

---

## ⚙️ Installation & Usage

```bash
git clone https://github.com/JohnsonJiang1996/Awesome-VLA4AD.git
cd Awesome-VLA4AD
# Browse papers, datasets & code samples in each folder
```

---

## 📜 Citation

If this project is useful in your work, we'd appreciate a star 🌟 and a citation of our paper.
```
@article{jiang2025vla4ad,
    title={A Survey on Vision-Language-Action Models for Autonomous Driving}, 
    author={Sicong Jiang and Zilin Huang and Kangan Qian and Ziang Luo and Tianze Zhu and Yang Zhong and Yihong Tang and Menglin Kong and Yunlong Wang and Siwen Jiao and Hao Ye and Zihao Sheng and Xin Zhao and Tuopu Wen and Zheng Fu and Sikai Chen and Kun Jiang and Diange Yang and Seongjin Choi and Lijun Sun},
    journal={arXiv preprint arXiv:2506.24044},
    year={2025}
}
```
