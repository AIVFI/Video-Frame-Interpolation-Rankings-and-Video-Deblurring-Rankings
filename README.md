# Vimeo90K: 36dB PSNR And Above - Video Frame Interpolation Models List

Looking for someone who has the knowledge, skills and willingness to test models from the following methods using **FloLPIPS** - probably the first and best metric specifically designed for video frame interpolation [[arXiv]](https://arxiv.org/abs/2207.08119) [[GitHub]](https://github.com/danielism97/flolpips) (originally announced July 2022).

Also looking for someone who has the knowledge, skills and willingness to test the **inference time** of the following models under identical test conditions, preferably for 1920x1080p video.

The ranking only contains the single best model in terms of PSNR for one method (paper).


| Rank | Model | PSNR (official) | PSNR (unofficial) | Originally announced (arXiv)| 
| :----:| :---- | :----: | :----: | :----: |
| 1 | JNMR | **37.09dB** [1] | - | June 2022 |
| 2 | VFIT-B | **36.96dB** [2] | - | November 2021 |
| 3 | MA-CSPA |  **36.76dB** [3] | - | March 2022 |
| 4 | TTVFI |  **36.54dB** [4] | - | July 2022 |
| 5 | VRT |  **36.53dB** [5] | - | June 2022 (VFI) |
| 6 | VFIformer |  **36.50dB** [6] | - | May 2022 |
| 7 | ST-MFNet | - [7] | **36.45dB** [1] | November 2021 |
| 8 | EAFI *L*ecc |  **36.38dB** [8] | - | July 2022 |
| 9 | FLAVR |  **36.25dB** [9] | - | December 2020 |
| 10 | IFRNet large |  **36.20dB** [10] | - | May 2022 |
| 11-12 | EBME-H∗ |  **36.19dB** [11] | - | June 2022 |
| 11-12 | RIFE-Large |  **36.19dB** [12] | - | November 2020 |
| 13 | ABME |  **36.18dB** [13] | - | August 2021 |
| 14 | EDC | - [14] | **36.14dB** [1] | February 2022 |
| 15 | SoftSplat *L*Lap |  **36.10dB** [15] | - | March 2020 |
| 16 | FILM-*L*1 |  **36.06dB** [16] | - | February 2022 |

[1] JNMR: Joint Non-linear Motion Regression for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2206.04231)  
[2] Video Frame Interpolation Transformer (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2111.13817) [[GitHub]](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer)  
[3] Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2203.10291)  
[4] TTVFI: Learning Trajectory-Aware Transformer for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.09048)  
[5] VRT: A Video Restoration Transformer [[arXiv]](https://arxiv.org/abs/2201.12288) [[GitHub]](https://github.com/JingyunLiang/VRT)  
[6] Video Frame Interpolation with Transformer (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2205.07230) [[GitHub]](https://github.com/dvlab-research/VFIformer)  
[7] ST-MFNet: A Spatio-Temporal Multi-Flow Network for Frame Interpolation (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2111.15483) [[GitHub]](https://github.com/danielism97/ST-MFNet)  
[8] Error-Aware Spatial Ensembles for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.12305)  
[9] FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation [[arXiv]](https://arxiv.org/abs/2012.08512) [[GitHub]](https://github.com/tarun005/FLAVR)  
[10] IFRNet: Intermediate Feature Refine Network for Efficient Frame Interpolation (CVPR 2022) [[arXiv]](https://arxiv.org/abs/2205.14620) [[GitHub]](https://github.com/ltkong218/IFRNet)  
[11] Enhanced Bi-directional Motion Estimation for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2206.08572)  
[12] Real-Time Intermediate Flow Estimation for Video Frame Interpolation (ECCV 2022) [[arXiv]](https://arxiv.org/abs/2011.06294) [[GitHub]](https://github.com/megvii-research/ECCV2022-RIFE)  
[13] Asymmetric Bilateral Motion Estimation for Video Frame Interpolation (ICCV 2021) [[arXiv]](https://arxiv.org/abs/2108.06815) [[GitHub]](https://github.com/JunHeum/ABME))  
[14] Enhancing Deformable Convolution based Video Frame Interpolation with Coarse-to-fine 3D CNN [[arXiv]](https://arxiv.org/abs/2202.07731) [[GitHub]](https://github.com/danielism97/EDC))  
[15] Softmax Splatting for Video Frame Interpolation (CVPR 2020) [[arXiv]](https://arxiv.org/abs/2003.05534)
 [[GitHub]](https://github.com/sniklaus/softmax-splatting)  
[16] FILM: Frame Interpolation for Large Motion (ECCV 2022) [[arXiv]](https://arxiv.org/abs/2202.04901) [[GitHub]](https://github.com/google-research/frame-interpolation)
