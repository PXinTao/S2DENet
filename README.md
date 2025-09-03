# S²DENet: Shallow Suppression and Deep Enhancement Network

# Code will be made available upon paper acceptance

## Overview

S²DENet introduces a depth-differentiated hierarchical processing paradigm that employs shallow suppression in noise-dominated early layers and deep enhancement in semantically-rich later layers. This approach achieves state-of-the-art performance with minimal computational overhead.

### Key Features
- **Ultra-Lightweight**: Only 0.05M/0.15M parameters (99% reduction vs existing methods)
- **High Performance**: SOTA results on 9/10 public ultrasound datasets
- **Real-Time Inference**: 81-82 FPS on NVIDIA RTX A8000
- **Clinical Ready**: Suitable for resource-constrained environments

## Architecture

### Core Components
- **Multi-order Differential Convolution (MDiffConv)**: High-frequency feature processing with depth-specific strategies
- **Differential Self-Attention (DiffSA)**: Noise-robust attention mechanism for structural information preservation
- **Hierarchical Design**: Specialized processing for different network depths

## Performance Comparison

| Method | AvgDice (%) | Params (M) | MACs (G) | FPS |
|--------|-------------|------------|----------|-----|
| U-Net | 74.59 | 34.53 | 65.52 | 87 |
| TransUNet | 84.92 | 105.28 | 24.67 | 59 |
| MobileUViT | 87.65 | 6.21 | 10.43 | 69 |
| **S²DENet** | **88.68** | **0.15** | **0.77** | **81** |
| **S²DENet-Tiny** | **87.44** | **0.05** | **0.27** | **82** |


## Datasets

Evaluated on 10 public ultrasound datasets:
- Breast: BUSI, BUSIS, BUS_BRA, UDIAT
- Kidney: KidneyUS
- Fetal: Fetal-HC  
- Carotid: CCAU
- Thyroid: DDTI
- Muscle: FALLMUD
- Cardiac: EchoNetED

## Citation

```bibtex
@article{s2denet2024,
  title={S²DENet: Shallow Suppression and Deep Enhancement Network for Ultrasound Image Segmentation},
  author={Pang, Xintao and Yang, Jinlin and Gao, Zhifan and others},
  journal={Preprint},
  year={2024}
}
```

## License

MIT License
