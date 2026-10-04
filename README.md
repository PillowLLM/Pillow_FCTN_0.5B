# Multi-Frequency FCTN Side-Diffusion Painting Model
## README.md

# Multi-Frequency Continuous Thought Network with Side Diffusion
**FCTN-SideDiff**
Hybrid Cognitive-Generative Architecture for Controllable Image Synthesis

## Overview
This repository implements a novel hybrid neural framework:
**Multi-Frequency FCTN cognitive backbone + independent side-branch diffusion decoder**.

FCTN acts as the intelligent thinking brain, performing multi-frequency spectral feature extraction, selective gated attention and adaptive memory reasoning. The side diffusion branch works as the rendering hand, refining local details, texture and color presentation. Two modules cooperate synchronously to achieve logic-structured, high-fidelity AI painting generation.

## Core Architecture
1. **Multi-Frequency Fourier VNN**
Decompose input embedding into low, medium and high frequency bands. Capture global outline, middle layout and fine granular features via separate frequency projection branches, fuse multi-scale spectral information.

2. **Selective Cognitive Mechanism**
- Gated selective attention: dynamically activate or shut down attention computation according to task complexity
- Adaptive memory unit: store historical reasoning states, realize step-wise continuous thought iteration

3. **Side Independent Diffusion Decoder**
Detached diffusion UNet placed at side branch, no interference with main cognitive flow. Take hierarchical structural latent features output by FCTN as conditional guidance, complete noise reduction and local detail painting.

4. **Synchronous Linkage Strategy**
FCTN reasoning steps correspond one-to-one with diffusion sampling steps. Structural cognition guides visual rendering progressively, realizing human-like "think first, draw later" generation logic.

## Key Features
- ✅ Multi-frequency domain joint encoding, richer spectral representation
- ✅ Selective activation, flexible computation cost control
- ✅ Separated cognition and rendering, stable hybrid generation
- ✅ Step-wise guided diffusion, strong structural controllability
- ✅ Original self-designed network, no identical public architecture

## Model Structure
```
Input Embedding
        ↓
Multi-Frequency Fourier VNN (3 frequency branches)
        ↓
Selective Gated Attention + Dynamic Memory
        ↓
Step-wise Structural Latent Sequence
        ↘
Side Diffusion UNet (Local detail refinement)
        ↓
Final Generated Image
```

## Environment Requirements
```
torch >= 2.0
numpy
tqdm
```

## Quick Start
### 1. Model Initialization
```python
from model import MultiFreqFCTN_SideDiffusion
model = MultiFreqFCTN_SideDiffusion(
    text_dim=512,
    latent_dim=512,
    img_size=64,
    think_steps=8,
    diffusion_steps=1000
)
```

### 2. Training Mode
```python
loss = model(text_embedding, ground_truth_image)
loss.backward()
```

### 3. Image Generation Mode
```python
gen_image = model(text_embedding)
```

## Application Scenarios
- Text-to-image generation
- Sketch structure guided painting
- Multi-detail controllable visual synthesis
- Sequential cognitive generative tasks

## License
Open source for academic research and personal development.

---

<div align="center">

<a href="https://github.com/PillowLLM/Pillow_FCTN_0.5B">
  <img width="100%" src="https://alittlecatgirlpanel.yxp.hk/card?repo=PillowLLM/Pillow_FCTN_0.5B" alt="gh-card · PillowLLM/Pillow_FCTN_0.5B" />
</a>

<sub>Powered by <a href="https://alittlecatgirlpanel.yxp.hk"><b>gh-card</b></a> · 粉色手写体 README 仓库名片</sub>

</div>
