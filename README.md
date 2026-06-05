# DiffSensei-Unofficial

> Unofficial PyTorch implementation starter for **DiffSensei: Bridging Multi-Modal LLMs and Diffusion Models for Customized Manga Generation** (CVPR 2025).
>
> If this repo saves you reading / reproduction time, please star it and follow [@StaryMoon](https://github.com/StaryMoon). I am building honest open reproduction starters for recent CVPR papers.

## Status

This repository is an **independent, unofficial, work-in-progress starter**.

- Paper: [DiffSensei: Bridging Multi-Modal LLMs and Diffusion Models for Customized Manga Generation](https://openaccess.thecvf.com/content/CVPR2025/html/Wu_DiffSensei_Bridging_Multi-Modal_LLMs_and_Diffusion_Models_for_Customized_Manga_CVPR_2025_paper.html)
- Venue: CVPR 2025
- Reproduction status: **benchmarks are not reproduced yet**
- Relationship to authors: this repo is not official and is not affiliated with the paper authors.

## What Is Implemented

This v0.1.0 starter implements a compact, readable scaffold inspired by the paper:

- separate visual and language token pathways
- cross-modal fusion block
- understanding and generation heads
- toy contrastive/generation loss
- smoke-test script

The goal is to make the high-level idea easy to inspect, fork, and improve.

## What Is Not Implemented Yet

- large language model backbone
- image diffusion backend
- large-scale instruction tuning
- official evaluation protocol

## Quick Start

```bash
git clone https://github.com/StaryMoon/DiffSensei-Unofficial.git
cd DiffSensei-Unofficial
pip install -r requirements.txt
python scripts/smoke_test.py
```

Expected output includes:

```text
loss: ...
logits: torch.Size([2, 8, 32])
```

## Minimal Usage

```python
import torch
from diffsensei_unofficial import UnofficialStarter

image = torch.rand(2, 3, 64, 64)
model = UnofficialStarter(kind="vlm")
out = model(image)
```

## Roadmap

- [ ] Replace toy modules with a closer implementation of the paper.
- [ ] Add dataset loader and config files.
- [ ] Add metric scripts and visualization.
- [ ] Reproduce a small benchmark or ablation table.
- [ ] Add pretrained weights once experiments are stable.

## Search Tags

cvpr-2025, manga-generation, diffusion, mllm, pytorch, unofficial-implementation

## Citation

Please cite the original paper if you use the method. This repo is only an unofficial starter and does not replace the paper.

## License

MIT License. The original paper and official materials remain owned by their respective authors / publishers.
