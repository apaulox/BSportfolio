# Research Portfolio

**Undergraduate Research | Audio, Speech, Computer Vision & Multimodal Learning**

I am an undergraduate student in the Department of Electronic Engineering at Hanyang University, interested in learning representations from audio and visual signals. My current interests include **audio-visual correspondence**, **spatial audio**, **self-supervised representation learning**, and **robust audio classification**.

This repository is a **research-oriented portfolio**, not a release of all experimental code. It highlights research questions, methodology, evidence, and limitations. Some implementation repositories remain private while results and permissions are reviewed.

## Selected Projects

### 1. Binaural Audio Generation via Audio Visual Multi head Aggregation
**Research focus:** Visually guided mono-to-binaural audio generation with separate complementary semantic/spatial representations.

- Investigated separate semantic (image–mono audio) and spatial (image–binaural cues) correspondence objectives.
- Explored frozen DINOv2/DINOv3 visual backbones, dense contrastive similarities, multi-head architectures, and visually conditioned reconstruction.
- Compared similarity aggregation, backbone choice, decoder conditioning, and seen versus category-unseen evaluations.
- Studied what the learned heads encode using retrieval tasks and visual/audio interventions.

**Selected evidence:** In one recorded seen-category ablation, a multi-head product-then-pool configuration yielded **0.8173 STFT distance** and **0.1284 envelope distance**. These metrics are specific to that evaluation setup; a separate category-unseen test showed a substantial generalization gap.

[Project overview and limitations](projects/av-spatial-correspondence.md)

### 2. Music Deepfake Detection
**Research focus:** Detecting AI-generated or manipulated music and vocals.

- Investigated speech and music detection components, including pretrained audio representations and source separation.
- Experimented with EAT/XLS-R-based pipelines and HTDemucs-based input processing, fusion, and inference packaging.
- Emphasized reproducible evaluation, controlled comparisons, and deployment constraints.

[Project overview](projects/music-deepfake-detection.md)

### 3. Wafer Defect Classification in scarse data situations
**Research focus:** Visual defect recognition under dataset/domain differences.

- Trained and compared ResNet and EfficientNet image classifiers on five wafer image classes.
- Studied the value of adding source-domain training data while evaluating on a target-domain validation set.
- Explored augmentation and model-capacity tradeoffs.

[Project overview](projects/wafer-defect-classification.md)

## Research Interests

- Audio-visual and cross-modal representation learning
- Speech/audio signal processing and spatial audio
- Self-supervised and contrastive learning
- Robust classification, generalization, and experimental methodology

## Technical Background

**Languages & tools:** Python, PyTorch, Linux/WSL, Git, CUDA-based GPU workflows  
**Methods:** STFT-based audio processing, contrastive objectives, transformer visual backbones, convolutional networks, ablations, retrieval/evaluation analysis

## Code, Provenance & Reproducibility

- This public portfolio contains summaries rather than private datasets, model weights, or confidential training artifacts.
- Results are reported with their evaluation contexts; a seen-category result is **not** evidence of category-unseen generalization.
- Research built on prior work is described as such, and original implementations should be credited to their respective authors.
- **Related public reference implementation:** [CCStereo](https://github.com/apaulox/CCStereo). This repository contains a copy of the CCStereo research implementation; it should **not** be interpreted as my original publication.
- Project code and additional experiment material may be shared when appropriate permissions and release reviews are complete.

---
*This portfolio is maintained for academic research introductions and graduate laboratory applications.*
