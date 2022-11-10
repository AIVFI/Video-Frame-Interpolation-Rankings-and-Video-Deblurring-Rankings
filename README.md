# Rankings of Video Frame Interpolation Models Based on PSNR, SSIM, LPIPS, FloLPIPS Metrics

Currently available 3 rankings based on the Vimeo90K benchmarks. Each Ranking contains only the single best model for one method (paper).

A request to researchers: please use in the evaluation of your models **FloLPIPS** - probably the first and best metric specifically designed for video frame interpolation [[arXiv]](https://arxiv.org/abs/2207.08119) [[GitHub]](https://github.com/danielism97/flolpips) (originally announced July 2022).

### Vimeo90K benchmark (septuplet test set) - PSNR metric (entry threshold is 36dB)

| Rank | Model | PSNR | Originally announced | Official repository | ncnn | VapourSynth and AviSynth+ |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | JNMR | **37.09dB** [^1] | June 2022 [^1] | - | - | - |
| 2 | VFIT-B | **36.96dB** [^2] | November 2021 [^2] | [PyTorch](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) ![Github stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 3 | VRT |  **36.53dB** [^5] | June 2022 (VFI) [^5] | [PyTorch](https://github.com/JingyunLiang/VRT) ![Github stars](https://img.shields.io/github/stars/JingyunLiang/VRT) | - | - |
| 4 | MA-CSPA septuplet-trained |  **36.50dB** [^3] | March 2022 [^3] | - | - | - |
| 5 | ST-MFNet | **36.45dB** [^1] | November 2021 [^7] | [PyTorch](https://github.com/danielism97/ST-MFNet) ![Github stars](https://img.shields.io/github/stars/danielism97/ST-MFNet) | - | - |
| 6 | FLAVR |  **36.25dB** [^9] | December 2020 [^9] | [PyTorch](https://github.com/tarun005/FLAVR) ![Github stars](https://img.shields.io/github/stars/tarun005/FLAVR) | - | - |
| 7 | DBVI |  **36.17dB** [^17] | 2022 [^17] | [PyTorch](https://github.com/Oceanlib/DBVI) ![Github stars](https://img.shields.io/github/stars/Oceanlib/DBVI) | - | - |
| 8 | EDC | **36.14dB** [^1] | February 2022 [^14] | [PyTorch](https://github.com/danielism97/EDC) ![Github stars](https://img.shields.io/github/stars/danielism97/EDC) | - | - |

### Vimeo90K benchmark (triplet test set) - PSNR metric (entry threshold is 36dB)

| Rank | Model | PSNR | Originally announced | Official repository | ncnn | VapourSynth and AviSynth+ |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | MA-CSPA triplet-trained |  **36.76dB** [^3] | March 2022 [^3] | - | - | - |
| 2 | TTVFI |  **36.54dB** [^4] | July 2022 [^4] | - | - | - |
| 3 | VFIformer |  **36.50dB** [^6] | May 2022 [^6] | [PyTorch](https://github.com/dvlab-research/VFIformer) ![Github stars](https://img.shields.io/github/stars/dvlab-research/VFIformer) | - | - |
| 4 | UPR-Net LARGE |  **36.42dB** [^18] | November 2022 [^18] | - | - | - |
| 5 | EAFI *L*ecc |  **36.38dB** [^8] | July 2022 [^8] | - | - | - |
| 6 | IFRNet large |  **36.20dB** [^10] | May 2022 [^10] | [PyTorch](https://github.com/ltkong218/IFRNet) ![Github stars](https://img.shields.io/github/stars/ltkong218/IFRNet) | [ncnn](https://github.com/nihui/ifrnet-ncnn-vulkan) ![Github stars](https://img.shields.io/github/stars/nihui/ifrnet-ncnn-vulkan) | - |
| 7-8 | EBME-H∗ |  **36.19dB** [^11] | June 2022 [^11] | [PyTorch](https://github.com/srcn-ivl/EBME) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/EBME) | - | - |
| 7-8 | RIFE-Large |  **36.19dB** [^12] | November 2020 [^12] | [PyTorch](https://github.com/megvii-research/ECCV2022-RIFE) ![Github stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE) | [ncnn](https://github.com/nihui/rife-ncnn-vulkan) ![Github stars](https://img.shields.io/github/stars/nihui/rife-ncnn-vulkan) | [VapourSynth&TensorRT](https://github.com/HolyWu/vs-rife) ![Github stars](https://img.shields.io/github/stars/HolyWu/vs-rife) [VapourSynth&ncnn](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan) ![Github stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan) [VapourSynth&ncnn](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) ![Github stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)  [AviSynth+&ncnn](https://github.com/Asd-g/AviSynthPlus-RIFE) ![Github stars](https://img.shields.io/github/stars/Asd-g/AviSynthPlus-RIFE) |
| 9 | ABME |  **36.18dB** [^13] | August 2021 [^13] | [PyTorch](https://github.com/JunHeum/ABME) ![Github stars](https://img.shields.io/github/stars/JunHeum/ABME) | - | - |
| 10 | SoftSplat *L*Lap |  **36.10dB** [^15] | March 2020 [^15] | [PyTorch](https://github.com/sniklaus/softmax-splatting) ![Github stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting) | - | - |
| 11 | FILM-*L*1 |  **36.06dB** [^16] | February 2022 [^16] | [TensorFlow](https://github.com/google-research/frame-interpolation) ![Github stars](https://img.shields.io/github/stars/google-research/frame-interpolation) | - | - |

### Vimeo90K benchmark (triplet test set) - SSIM metric (entry threshold is 0.9800)

| Rank | Model | SSIM | Originally announced | Official repository | ncnn | VapourSynth and AviSynth+ |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | TTVFI |  **0.9819** [^4] | July 2022 [^4] | - | - | - |
| 2 | VFIformer |  **0.9816** [^6] | May 2022 [^6] | [PyTorch](https://github.com/dvlab-research/VFIformer) ![Github stars](https://img.shields.io/github/stars/dvlab-research/VFIformer) | - | - |
| 3 | UPR-Net LARGE |  **0.9815** [^18] | November 2022 [^18] | - | - | - |
| 4-5 | EBME-H∗ |  **0.981** [^11] | June 2022 [^11] | [PyTorch](https://github.com/srcn-ivl/EBME) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/EBME) | - | - |
| 4-5 | RIFE-Large |  **0.981** [^12] | November 2020 [^12] | [PyTorch](https://github.com/megvii-research/ECCV2022-RIFE) ![Github stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE) | [ncnn](https://github.com/nihui/rife-ncnn-vulkan) ![Github stars](https://img.shields.io/github/stars/nihui/rife-ncnn-vulkan) | [VapourSynth&TensorRT](https://github.com/HolyWu/vs-rife) ![Github stars](https://img.shields.io/github/stars/HolyWu/vs-rife) [VapourSynth&ncnn](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan) ![Github stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan) [VapourSynth&ncnn](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) ![Github stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)  [AviSynth+&ncnn](https://github.com/Asd-g/AviSynthPlus-RIFE) ![Github stars](https://img.shields.io/github/stars/Asd-g/AviSynthPlus-RIFE) |
| 6 | IFRNet large |  **0.9808** [^10] | May 2022 [^10] | [PyTorch](https://github.com/ltkong218/IFRNet) ![Github stars](https://img.shields.io/github/stars/ltkong218/IFRNet) | [ncnn](https://github.com/nihui/ifrnet-ncnn-vulkan) ![Github stars](https://img.shields.io/github/stars/nihui/ifrnet-ncnn-vulkan) | - |
| 7 | ABME |  **0.9805** [^13] | August 2021 [^13] | [PyTorch](https://github.com/JunHeum/ABME) ![Github stars](https://img.shields.io/github/stars/JunHeum/ABME) | - | - |
| 8 | MA-CSPA triplet-trained |  **0.980** [^3] | March 2022 [^3] | - | - | - |

[^1]: JNMR: Joint Non-linear Motion Regression for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2206.04231)
[^2]: Video Frame Interpolation Transformer (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2111.13817)
[^3]: Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2203.10291)
[^4]: TTVFI: Learning Trajectory-Aware Transformer for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.09048)
[^5]: VRT: A Video Restoration Transformer [[arXiv]](https://arxiv.org/abs/2201.12288)
[^6]: Video Frame Interpolation with Transformer (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2205.07230)
[^7]: ST-MFNet: A Spatio-Temporal Multi-Flow Network for Frame Interpolation (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2111.15483)
[^8]: Error-Aware Spatial Ensembles for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.12305)
[^9]: FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation [[arXiv]](https://arxiv.org/abs/2012.08512)
[^10]: IFRNet: Intermediate Feature Refine Network for Efficient Frame Interpolation (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2205.14620)
[^11]: Enhanced Bi-directional Motion Estimation for Video Frame Interpolation (WACV 2023) [[arXiv]](https://arxiv.org/abs/2206.08572)
[^12]: Real-Time Intermediate Flow Estimation for Video Frame Interpolation (ECCV 2022) [[arXiv]](https://arxiv.org/abs/2011.06294)
[^13]: Asymmetric Bilateral Motion Estimation for Video Frame Interpolation (ICCV 2021) [[arXiv]](https://arxiv.org/abs/2108.06815)
[^14]: Enhancing Deformable Convolution based Video Frame Interpolation with Coarse-to-fine 3D CNN (ICIP'2022) [[arXiv]](https://arxiv.org/abs/2202.07731)
[^15]: Softmax Splatting for Video Frame Interpolation (CVPR 2020) [[arXiv]](https://arxiv.org/abs/2003.05534)
[^16]: FILM: Frame Interpolation for Large Motion (ECCV 2022) [[arXiv]](https://arxiv.org/abs/2202.04901)
[^17]: Deep Bayesian Video Frame Interpolation (ECCV 2022) [[ECVA]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/1287_ECCV_2022_paper.php)
[^18]: A Unified Pyramid Recurrent Network for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2211.03456) 
