# <p align=center>Video Frame Interpolation Rankings<br />and Video Deblurring Rankings</p>

Researchers! Please develope joint video deblurring and frame interpolation models, use the best method for dealing with time-to-location ambiguity between two input frames, which the [BiM-VFI](https://arxiv.org/abs/2412.11365) currently has and train at least one of your models on [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison), also called Gram matrix loss (the best perceptual loss function).

#### Loss Function Comparison:
![FILM - Loss Functions Ablation](https://film-net.github.io/static/images/loss_ablation.png)
Source: FILM - Loss Functions Ablation https://film-net.github.io/

<img alt="MoSt-DSA - Loss Function Comparison" src="MoSt-DSA.png">
Source: MoSt-DSA - Loss Function Comparison https://arxiv.org/html/2407.07078

## <p align=center>List of Rankings</p>
<p align=center>Each ranking includes only the best model for one method.</p>  
<p align=center>The rankings exclude all event-based and spike-guided models.</p>

### Joint Video Deblurring and Frame Interpolation Rankings
1. :crown: **RBI with real motion blur✔️: LPIPS😍** (no data)  
*This will be the King of all rankings. We look forward to ambitious researchers.*
1. [**RBI with real motion blur✔️: PSNR😞>=28.5dB**](#rbi-with-real-motion-blur%EF%B8%8F-psnr285db)
### Video Deblurring Rankings
- (to do)
### Video Frame Interpolation Rankings
1. [**X-TEST (×8): LPIPS😍<=0.098**](#x-test-8-lpips0098)
1. [**SNU-FILM-arb Extreme (×16): LPIPS😍<=0.095**](#snu-film-arb-extreme-16-lpips0095)
1. [**SNU-FILM-arb Hard (×8): LPIPS😍<=0.048**](#snu-film-arb-hard-8-lpips0048)
1. [**SNU-FILM-arb Medium (×4): LPIPS😍<=0.026**](#snu-film-arb-medium-4-lpips0026)
1. [**SNU-FILM Extreme (×2): LPIPS😍<=0.1099**](#snu-film-extreme-2-lpips01099)
1. [**SNU-FILM Hard (×2): LPIPS😍<=0.052**](#snu-film-hard-2-lpips0052)
1. [**SNU-FILM Medium (×2): LPIPS😍<=0.024**](#snu-film-medium-2-lpips0024)
### Video Frame Interpolation Rankings that will no longer be updated
1. [**Vimeo-90K triplet: LPIPS😍<=0.018**](#vimeo-90k-triplet-lpips0018)
1. [**Vimeo-90K triplet: LPIPS😍(SqueezeNet)<=0.014**](#vimeo-90k-triplet-lpipssqueezenet0014)
1. [**Vimeo-90K triplet: PSNR😞>=36dB**](#vimeo-90k-triplet-psnr36db)
1. [**Vimeo-90K septuplet: PSNR😞>=36dB**](#vimeo-90k-septuplet-psnr36db)
### Appendices
- [**Appendix 1: Runtime**](#appendix-1-runtime)
- **Appendix 2: Rules for qualifying models for the rankings** (to do)
- [**Appendix 3: Metrics selection for the rankings**](#appendix-3-metrics-selection-for-the-rankings)
- [**Appendix 4: List of all research papers from the above rankings**](#appendix-4-list-of-all-research-papers-from-the-above-rankings)

--------------------

## RBI with real motion blur✔️: PSNR😞>=28.5dB
📝 Note: Pre-BiT++ is pre-trained on Adobe240 and then fine-tuned on RBI.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;PSNR&nbsp;↑&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhong_Blur_Interpolation_Transformer_for_Real-World_Motion_From_Blur_CVPR_2023_paper.html)<br />Table 1&6<br />BiT |
|:---:|:---:|:---:|
| 1 | **Pre-BiT++**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhong_Blur_Interpolation_Transformer_for_Real-World_Motion_From_Blur_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/BiT)](https://github.com/zzh-tech/BiT) | **31.32** {3} |
| 2 | **DeMFI-Net**<sub>*rb*</sub>**(5,3)**<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4406_ECCV_2022_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/DeMFI)](https://github.com/JihyongOh/DeMFI) | **29.03** {4} |
| 3 | **PRF<sub>4</sub>** -*Large*<br />[![TIP](https://img.shields.io/badge/2020-TIP-dba2a7)](https://ieeexplore.ieee.org/document/9257179) [![GitHub Stars](https://img.shields.io/github/stars/laomao0/BIN)](https://github.com/laomao0/BIN) | **28.55** {5} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## X-TEST (×8): LPIPS😍<=0.098
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![OpenReview](https://img.shields.io/badge/OpenReview-8c1b13)](https://openreview.net/forum?id=S6fd7X47Ra)<br />Table 1<br />DvP | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 4<br />BiM-VFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.08680)<br />Table 4&7<br />GIMM-VFI |
|:---:|:---:|:---:|:---:|:---:|
| 1 | **DvP+**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3681555) | **0.062** {4} | - | - |
| 2 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | **0.068** {2} | - |
| 3 | **M2M-PWC**<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Hu_Many-to-Many_Splatting_for_Efficient_Video_Frame_Interpolation_CVPR_2022_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/feinanshan/M2M_VFI)](https://github.com/feinanshan/M2M_VFI) | **0.086** {2} | **0.080** {2} | **0.158** {2} |
| 4 | **XVFI (S**<sub>*tst*</sub>**=5)**<br />[![ICCV](https://img.shields.io/badge/2021-ICCV-fcb900)](https://openaccess.thecvf.com/content/ICCV2021/html/Sim_XVFI_eXtreme_Video_Frame_Interpolation_ICCV_2021_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/XVFI)](https://github.com/JihyongOh/XVFI) | **0.089** {2} | - | - |
| 5 | **UPR-Net LARGE**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_A_Unified_Pyramid_Recurrent_Network_for_Video_Frame_Interpolation_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net)](https://github.com/srcn-ivl/UPR-Net) | - | **0.093** {2} | **0.154** {2} |
| 6-7 | **GIMM-VFI-F-P**<br />[![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html) [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) | - | - | **0.098** {2} |
| 6-7 | **IA-Clearer [D,R]<sub>u</sub> AMT-S**<br />[![ECCV](https://img.shields.io/badge/2024-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/4908_ECCV_2024_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/InterpAny-Clearer)](https://github.com/zzh-tech/InterpAny-Clearer) | - | **0.098** {2} | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM-arb Extreme (×16): LPIPS😍<=0.095
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.08680)<br />Table 4&7<br />GIMM-VFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 1<br />BiM-VFI |
|:---:|:---:|:---:|:---:|
| 1 | **GIMM-VFI-F-P**<br />[![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html) [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) | **0.058** {2} | - |
| 2 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | **0.070** {2} |
| 3 | **M2M-PWC**<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Hu_Many-to-Many_Splatting_for_Efficient_Video_Frame_Interpolation_CVPR_2022_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/feinanshan/M2M_VFI)](https://github.com/feinanshan/M2M_VFI) | **0.112** {2} | **0.089** {2} |
| 4 | **UPR-Net LARGE**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_A_Unified_Pyramid_Recurrent_Network_for_Video_Frame_Interpolation_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net)](https://github.com/srcn-ivl/UPR-Net) | **0.111** {2} | **0.092** {2} |
| 5 | **IA-Clearer [D,R]<sub>u</sub> IFRNet**<br />[![ECCV](https://img.shields.io/badge/2024-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/4908_ECCV_2024_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/InterpAny-Clearer)](https://github.com/zzh-tech/InterpAny-Clearer) | - | **0.095** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM-arb Hard (×8): LPIPS😍<=0.048
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.08680)<br />Table 7<br />GIMM-VFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 1<br />BiM-VFI |
|:---:|:---:|:---:|:---:|
| 1 | **GIMM-VFI-F-P**<br />[![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html) [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) | **0.030** {2} | - |
| 2 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | **0.039** {2} |
| 3 | **IA-Clearer [D,R]<sub>u</sub> IFRNet**<br />[![ECCV](https://img.shields.io/badge/2024-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/4908_ECCV_2024_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/InterpAny-Clearer)](https://github.com/zzh-tech/InterpAny-Clearer) | - | **0.048** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM-arb Medium (×4): LPIPS😍<=0.026
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.08680)<br />Table 7<br />GIMM-VFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 1<br />BiM-VFI |
|:---:|:---:|:---:|:---:|
| 1 | **GIMM-VFI-R-P**<br />[![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html) [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) | **0.016** {2} | - |
| 2 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | **0.023** {2} |
| 3 | **IA-Clearer [D,R]<sub>u</sub> IFRNet**<br />[![ECCV](https://img.shields.io/badge/2024-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/4908_ECCV_2024_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/InterpAny-Clearer)](https://github.com/zzh-tech/InterpAny-Clearer) | - | **0.026** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM Extreme (×2): LPIPS😍<=0.1099
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380)<br />Table 1<br />HFD | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html)<br />Table 1<br />UGFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.17256)<br />Table 1<br />MoMo | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 2<br />BiM-VFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![OpenReview](https://img.shields.io/badge/OpenReview-8c1b13)](https://openreview.net/forum?id=S6fd7X47Ra)<br />Table 2<br />DvP | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2503.15831)<br />Table 1<br />EDEN | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2405.05953)<br />Table 1<br />CBBD |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | **HFD** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380) | **0.0839** {2} | - | - | - | - | - | - |
| 2 | **UGFI 𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | - | **0.0864** {2} | - | - | - | - | - |
| 3 | **MoMo** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://ojs.aaai.org/index.php/AAAI/article/view/32486) [![GitHub Stars](https://img.shields.io/github/stars/JHLew/MoMo)](https://github.com/JHLew/MoMo) | - | - | **0.0872** {2} | - | - | - | - |
| 4 | **FILM-𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) | - | **0.0899** {2} | **0.0889** {2} | - | - | - | - |
| 5 | **PerVFI**<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Perception-Oriented_Video_Frame_Interpolation_via_Asymmetric_Blending_CVPR_2024_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/mulns/PerVFI)](https://github.com/mulns/PerVFI) | **0.0901** {2} | - | **0.0902** {2} | - | - | - | - |
| 6-7 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | - | - | **0.097** {2} | - | - | - |
| 6-7 | **DvP+**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3681555) | - | - | - | - | **0.097** {4} | - | - |
| 8 | **EDEN**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2503.15831) [![GitHub Stars](https://img.shields.io/github/stars/bbldCVer/EDEN)](https://github.com/bbldCVer/EDEN) | - | - | - | - | - | **0.0986** {2} | - |
| 9 | **CBBD**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3680961) [![GitHub Stars](https://img.shields.io/github/stars/ZonglinL/ConsecutiveBrownianBridge)](https://github.com/ZonglinL/ConsecutiveBrownianBridge) | **0.1040** {2} | - | - | - | - | **0.1101** {2} | **0.104** {2} |
| 10 | **EMA-VFI**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Extracting_Motion_and_Appearance_via_Inter-Frame_Attention_for_Efficient_Video_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI)](https://github.com/MCG-NJU/EMA-VFI) | **0.1099** {2} | - | **0.1099** {2} | **0.113** {2} | **0.119** {2} | - | **0.114** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM Hard (×2): LPIPS😍<=0.052
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380)<br />Table 1<br />HFD | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![OpenReview](https://img.shields.io/badge/OpenReview-8c1b13)](https://openreview.net/forum?id=S6fd7X47Ra)<br />Table 2<br />DvP | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.17256)<br />Table 1<br />MoMo | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html)<br />Table 1<br />UGFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2405.05953)<br />Table 1<br />CBBD | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 2<br />BiM-VFI |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | **HFD** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380) | **0.0405** {2} | - | - | - | - | - |
| 2 | **DvP+**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3681555) | - | **0.041** {4} | - | - | - | - |
| 3 | **MoMo** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://ojs.aaai.org/index.php/AAAI/article/view/32486) [![GitHub Stars](https://img.shields.io/github/stars/JHLew/MoMo)](https://github.com/JHLew/MoMo) | - | - | **0.0419** {2} | - | - | - |
| 4 | **UGFI 𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | - | - | - | **0.0420** {2} | - | - |
| 5 | **FILM-𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) | - | - | **0.0429** {2} | **0.0434** {2} | - | - |
| 6 | **CBBD**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3680961) [![GitHub Stars](https://img.shields.io/github/stars/ZonglinL/ConsecutiveBrownianBridge)](https://github.com/ZonglinL/ConsecutiveBrownianBridge) | **0.0467** {2} | - | - | - | **0.047** {2} | - |
| 7 | **PerVFI**<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Perception-Oriented_Video_Frame_Interpolation_via_Asymmetric_Blending_CVPR_2024_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/mulns/PerVFI)](https://github.com/mulns/PerVFI) | **0.0480** {2} | - | **0.0561** {2} | - | - | - |
| 8 | **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | - | - | - | - | - | **0.052** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## SNU-FILM Medium (×2): LPIPS😍<=0.024
📝 Note: This ranking has the most up-to-date layout.
| RK | Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380)<br />Table 1<br />HFD | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![OpenReview](https://img.shields.io/badge/OpenReview-8c1b13)](https://openreview.net/forum?id=S6fd7X47Ra)<br />Table 2<br />DvP | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.17256)<br />Table 1<br />MoMo | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html)<br />Table 1<br />UGFI | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2405.05953)<br />Table 1<br />CBBD | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.}<br />[![arXiv](https://img.shields.io/badge/2020-arXiv-b31b1b)](https://arxiv.org/abs/2006.08070)<br />Table 6<br />EDSC |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | **HFD** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380) | **0.0191** {2} | - | - | - | - | - |
| 2 | **DvP+**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3681555) | - | **0.020** {4} | - | - | - | - |
| 3 | **MoMo** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://ojs.aaai.org/index.php/AAAI/article/view/32486) [![GitHub Stars](https://img.shields.io/github/stars/JHLew/MoMo)](https://github.com/JHLew/MoMo) | - | - | **0.0202** {2} | - | - | - |
| 4 | **UGFI 𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | - | - | - | **0.0209** {2} | - | - |
| 5 | **FILM-𝓛<sub>*S*</sub>** [![Style loss](https://img.shields.io/badge/Style_loss-000000)](#loss-function-comparison)<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) | - | - | **0.0213** {2} | **0.0215** {2} | - | - |
| 6 | **CBBD**<br />[![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3680961) [![GitHub Stars](https://img.shields.io/github/stars/ZonglinL/ConsecutiveBrownianBridge)](https://github.com/ZonglinL/ConsecutiveBrownianBridge) | **0.0274** {2} | - | - | - | **0.022** {2} | - |
| 7-8 | **EDSC-𝓛<sub>*F*</sub>**<br />[![TPAMI](https://img.shields.io/badge/2021-TPAMI-fefd02)](https://ieeexplore.ieee.org/document/9501506) [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch)](https://github.com/Xianhang/EDSC-pytorch) | - | - | - | - | - | **0.024** {2} |
| 7-8 | **SepConv - 𝓛<sub>*F*</sub>**<br />[![ICCV](https://img.shields.io/badge/2017-ICCV-fcb900)](https://openaccess.thecvf.com/content_iccv_2017/html/Niklaus_Video_Frame_Interpolation_ICCV_2017_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/sepconv-slomo)](https://github.com/sniklaus/sepconv-slomo) | - | - | - | - | - | **0.024** {2} |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: LPIPS😍<=0.018
| RK | &nbsp;&nbsp;&nbsp;&nbsp;Model&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;LPIPS&nbsp;↓&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.} | Training<br />dataset | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | EAFI-𝓛<sub>*ecp*</sub><br />[![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2207.12305) |  **0.012** {2}<br />[![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2207.12305) | Vimeo-90K triplet | - | EAFI-𝓛<sub>*ecp*</sub> | - |
| 2 | UGFI 𝓛<sub>*S*</sub><br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | **0.0126** {2}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | Vimeo-90K triplet | - | UGFI 𝓛<sub>*S*</sub> | - |
| 3 | SoftSplat - 𝓛<sub>*F*</sub><br />[![CVPR](https://img.shields.io/badge/2020-CVPR-1e407f)](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) |  **0.013** {2}<br />[![CVPR](https://img.shields.io/badge/2020-CVPR-1e407f)](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting)](https://github.com/sniklaus/softmax-splatting) | SoftSplat - 𝓛<sub>*F*</sub> | - |
| 4 | FILM-𝓛<sub>*S*</sub><br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) | **0.0132** {2}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) | [FILM-𝓛<sub>*S*</sub>](https://github.com/google-research/frame-interpolation#pre-trained-models) | - |
| 5 | MoMo<br />[![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://arxiv.org/abs/2406.17256) | **0.0136** {2}<br />[![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://arxiv.org/abs/2406.17256) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/JHLew/MoMo)](https://github.com/JHLew/MoMo) | [MoMo](https://github.com/JHLew/MoMo#download-the-pretrained-model) | - |
| 6 | EDSC_s-𝓛<sub>*F*</sub><br />[![TPAMI](https://img.shields.io/badge/2021-TPAMI-fefd02)](https://ieeexplore.ieee.org/document/9501506) |  **0.016** {2}<br />[![arXiv](https://img.shields.io/badge/2020-arXiv-b31b1b)](https://arxiv.org/abs/2006.08070) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch)](https://github.com/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |
| 7 | CtxSyn - 𝓛<sub>*F*</sub><br />[![CVPR](https://img.shields.io/badge/2018-CVPR-1e407f)](https://openaccess.thecvf.com/content_cvpr_2018/html/Niklaus_Context-Aware_Synthesis_for_CVPR_2018_paper.html) | **0.017** {2}<br />[![CVPR](https://img.shields.io/badge/2020-CVPR-1e407f)](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) | proprietary | - | CtxSyn - 𝓛<sub>*F*</sub> | - |
| 8 | PerVFI<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Perception-Oriented_Video_Frame_Interpolation_via_Asymmetric_Blending_CVPR_2024_paper.html) | **0.018** {2}<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Perception-Oriented_Video_Frame_Interpolation_via_Asymmetric_Blending_CVPR_2024_paper.html) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/mulns/PerVFI)](https://github.com/mulns/PerVFI) | [PerVFI](https://github.com/mulns/PerVFI#-download-checkpoints) | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: LPIPS😍(SqueezeNet)<=0.014
| RK | Model | LPIPS ↓ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | CDFI w/ adaP/U |  **0.008** [^23] | March 2021 [^24] | [![GitHub Stars](https://img.shields.io/github/stars/tding1/CDFI)](https://github.com/tding1/CDFI) | - | - |
| 2 | EDSC_s-𝓛<sub>*F*</sub> |  **0.010** [^24] | June 2020 [^25] | [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch)](https://github.com/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |
| 3 | DRVI |  **0.013** [^26] | August 2021 [^26] | - | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: PSNR😞>=36dB
| RK | &nbsp;&nbsp;&nbsp;&nbsp;Model&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;PSNR&nbsp;↑&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.} | Originally<br />announced<br />or Training<br />dataset | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | MA-GCSPA-triplets<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) | **36.85** {2}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/redrock303/CVPR23-MA-GCSPA)](https://github.com/redrock303/CVPR23-MA-GCSPA) | - | - |
| 2 | VFIformer + HRFFM<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Lu_Video_Frame_Interpolation_With_Transformer_CVPR_2022_paper.html)<br />*ENH:*<br />[![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2312.15868) |  **36.69** {2}<br />[![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2312.15868) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/dvlab-research/VFIformer)](https://github.com/dvlab-research/VFIformer)<br />*ENH:*<br />- | - | - |
| 3 | LADDER-L<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2404.11108) | **36.65** {2}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2404.11108) | Vimeo-90K triplet | - | - | - |
| 4-5 | EMA-VFI |  **36.64dB** [^22] | March 2023 [^22] | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI)](https://github.com/MCG-NJU/EMA-VFI) | - | - |
| 4-5 | VFIMamba<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.02315) | **36.64** {2}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.02315) | Vimeo-90K triplet & X-TRAIN | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/VFIMamba)](https://github.com/MCG-NJU/VFIMamba) | - | - |
| 6 | IQ-VFI<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Hu_IQ-VFI_Implicit_Quadratic_Motion_Estimation_for_Video_Frame_Interpolation_CVPR_2024_paper.html) | **36.60** {2}<br />[![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Hu_IQ-VFI_Implicit_Quadratic_Motion_Estimation_for_Video_Frame_Interpolation_CVPR_2024_paper.html) | Vimeo-90K triplet | - | - | - |
| 7 | DQBC-Aug |  **36.57dB** [^36] | April 2023 [^36] | [![GitHub Stars](https://img.shields.io/github/stars/kinoud/DQBC)](https://github.com/kinoud/DQBC) | - | - |
| 8 | TTVFI |  **36.54dB** [^4] | July 2022 [^4] | [![GitHub Stars](https://img.shields.io/github/stars/ChengxuLiu/TTVFI)](https://github.com/ChengxuLiu/TTVFI) | - | - |
| 9 | AMT-G |  **36.53dB** [^31] | April 2023 [^31] | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NKU/AMT)](https://github.com/MCG-NKU/AMT) | - | - |
| 10 | AdaFNIO |  **36.50dB** [^19] | November 2022 [^19] | [![GitHub Stars](https://img.shields.io/github/stars/IDEAS-Lab-Purdue/AdaFNIO)](https://github.com/IDEAS-Lab-Purdue/AdaFNIO) | - | - |
| 11 | FGDCN-L |  **36.46dB** [^21] | November 2022 [^21] | [![GitHub Stars](https://img.shields.io/github/stars/lpcccc-cv/FGDCN)](https://github.com/lpcccc-cv/FGDCN) | - | - |
| 12 | VFIFT<br />[![MM](https://img.shields.io/badge/2023-MM-cc1962)](https://dl.acm.org/doi/10.1145/3581783.3612440) | **36.43** {2}<br />[![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2307.16144) | Vimeo-90K triplet | - | - | - |
| 13 | UPR-Net LARGE |  **36.42dB** [^18] | November 2022 [^18] | [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net)](https://github.com/srcn-ivl/UPR-Net) | - | - |
| 14 | EAFI-𝓛<sub>*ecc*</sub> |  **36.38dB** [^8] | July 2022 [^8] | - | EAFI-𝓛<sub>*ecp*</sub> | - |
| 15 | H-VFI-Large |  **36.37dB** [^20] | November 2022 [^20] | - | - | - |
| 16 | UGFI 𝓛<sub>1</sub><br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | **36.34** {2}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | Vimeo-90K triplet | - | UGFI 𝓛<sub>*S*</sub> | - |
| 17 | VFIT-B<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) | **36.33** {2}<br />[![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2307.16144) | ? | [![GitHub Stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer)](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 18 | SoftSplat - 𝓛<sub>*Lap*</sub> with ensemble |  **36.28dB** [^28] | March 2020 [^15] | [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting)](https://github.com/sniklaus/softmax-splatting) | SoftSplat - 𝓛<sub>*F*</sub> | - |
| 19 | ProBoost-Net (448x256)<br />[![TMM](https://img.shields.io/badge/2022-TMM-f6d6bd)](https://ieeexplore.ieee.org/document/10003662) | **36.23** {2}<br />[![TMM](https://img.shields.io/badge/2022-TMM-f6d6bd)](https://ieeexplore.ieee.org/document/10003662) | ? | - | - | - |
| 20 | NCM-Large |  **36.22dB** [^32] | July 2022 [^32] | - | - | - |
| 21-22 | IFRNet large |  **36.20dB** [^10] | May 2022 [^10] | [![GitHub Stars](https://img.shields.io/github/stars/ltkong218/IFRNet)](https://github.com/ltkong218/IFRNet) | - | - |
| 21-22 | RAFT-M2M++<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Hu_Many-to-Many_Splatting_for_Efficient_Video_Frame_Interpolation_CVPR_2022_paper.html)<br />*ENH:*<br />[![TPAMI](https://img.shields.io/badge/2024-TPAMI-fefd02)](https://ieeexplore.ieee.org/document/10294102) | **36.20** {2}<br />[![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2310.18946) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/feinanshan/M2M_VFI)](https://github.com/feinanshan/M2M_VFI) | - | - |
| 23-24 | EBME-H* |  **36.19dB** [^11] | June 2022 [^11] | [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/EBME)](https://github.com/srcn-ivl/EBME) | - | - |
| 23-24 | RIFE-Large<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/95_ECCV_2022_paper.php) |  **36.19** {2}<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/95_ECCV_2022_paper.php) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE)](https://github.com/megvii-research/ECCV2022-RIFE) | [Practical-RIFE 4.25](https://github.com/hzwer/Practical-RIFE#trained-model) | [![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/AmusementClub/vs-mlrt)<br />[![GitHub Stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt)](https://github.com/AmusementClub/vs-mlrt)<br />[![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/HolyWu/vs-rife)<br />[![GitHub Stars](https://img.shields.io/github/stars/HolyWu/vs-rife)](https://github.com/HolyWu/vs-rife)<br />[![ncnn](https://img.shields.io/badge/ncnn-0052d9)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />[![GitHub Stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 25 | ABME |  **36.18dB** [^13] | August 2021 [^13] | [![GitHub Stars](https://img.shields.io/github/stars/JunHeum/ABME)](https://github.com/JunHeum/ABME) | - | - |
| 26 | HiFI<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2410.11838) | **36.12** {2}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2410.11838) | *Pretraining*: Raw videos<br />*Training*: Vimeo-90K triplet & X-TRAIN | - | - | - |
| 27 | TDPNet<sub>*nv*</sub> w/o MRTM<br />[![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) | **36.069** {2}<br />[![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) | Vimeo-90K triplet | - | TDPNet | - |
| 28 | FILM-𝓛<sub>1</sub><br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) | **36.06** {2}<br />[![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) | Vimeo-90K triplet | [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) | [FILM-𝓛<sub>*S*</sub>](https://github.com/google-research/frame-interpolation#pre-trained-models) | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K septuplet: PSNR😞>=36dB
| RK | &nbsp;&nbsp;&nbsp;&nbsp;Model&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;PSNR&nbsp;↑&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.} | Originally<br />announced<br />or Training<br />dataset | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | Swin-VFI<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.11371) | **38.04** {6}<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.11371) | Vimeo-90K septuplet | - | - | - |
| 2 | JNMR | **37.19dB** [^1] | June 2022 [^1] | [![GitHub Stars](https://img.shields.io/github/stars/ruhig6/JNMR)](https://github.com/ruhig6/JNMR) | - | - |
| 3 | VFIT-B<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) | **36.96** {4}<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) | Vimeo-90K septuplet | [![GitHub Stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer)](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 4 | VRT<br />[![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2201.12288) |  **36.53** {4}<br />[![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2201.12288) | Vimeo-90K septuplet | [![GitHub Stars](https://img.shields.io/github/stars/JingyunLiang/VRT)](https://github.com/JingyunLiang/VRT) | - | - |
| 5 | ST-MFNet | **36.507dB** [^42] | November 2021 [^7] | [![GitHub Stars](https://img.shields.io/github/stars/danielism97/ST-MFNet)](https://github.com/danielism97/ST-MFNet) | - | - |
| 6 | EDENVFI PVT(15,15) | **36.387dB** [^42] | July 2023 [^42] | - | - | - |
| 7 | IFRNet<br />[![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Kong_IFRNet_Intermediate_Feature_Refine_Network_for_Efficient_Frame_Interpolation_CVPR_2022_paper.html) | **36.37** {2}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html) | Vimeo-90K septuplet | [![GitHub Stars](https://img.shields.io/github/stars/ltkong218/IFRNet)](https://github.com/ltkong218/IFRNet) | - | - |
| 8 | RN-VFI<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html) | **36.33** {4}<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html) | Vimeo-90K septuplet | - | - | - |
| 9 | FLAVR<br />[![WACV](https://img.shields.io/badge/2023-WACV-2e0094)](https://openaccess.thecvf.com/content/WACV2023/html/Kalluri_FLAVR_Flow-Agnostic_Video_Representations_for_Fast_Frame_Interpolation_WACV_2023_paper.html) |  **36.3** {4}<br />[![WACV](https://img.shields.io/badge/2023-WACV-2e0094)](https://openaccess.thecvf.com/content/WACV2023/html/Kalluri_FLAVR_Flow-Agnostic_Video_Representations_for_Fast_Frame_Interpolation_WACV_2023_paper.html) | Vimeo-90K septuplet | [![GitHub Stars](https://img.shields.io/github/stars/tarun005/FLAVR)](https://github.com/tarun005/FLAVR) | - | - |
| 10 | DBVI |  **36.17dB** [^17] | October 2022 [^17] | [![GitHub Stars](https://img.shields.io/github/stars/Oceanlib/DBVI)](https://github.com/Oceanlib/DBVI) | - | - |
| 11 | EDC | **36.14dB** [^1] | February 2022 [^14] | [![GitHub Stars](https://img.shields.io/github/stars/danielism97/EDC)](https://github.com/danielism97/EDC) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Appendix 1: Runtime
| Model <br />*Links:*<br />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;Repository&nbsp;&nbsp;&nbsp;&nbsp; | Runtime(s)<br />(×2)<br />A100<br />1280×768<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365)<br />Table 7<br />BiM-VFI |
|:---:|:---:|
| **BiM-VFI**<br />[![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) | **0.151** |
| **EMA-VFI**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Extracting_Motion_and_Appearance_via_Inter-Frame_Attention_for_Efficient_Video_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI)](https://github.com/MCG-NJU/EMA-VFI) | **0.104** |
| **GIMM-VFI-R**<br />[![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html) [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) | **0.494** |
| **UPR-Net LARGE**<br />[![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_A_Unified_Pyramid_Recurrent_Network_for_Video_Frame_Interpolation_CVPR_2023_paper.html) [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net)](https://github.com/srcn-ivl/UPR-Net) | **0.053** |

## Appendix 3: Metrics selection for the rankings

Currently, the most commonly used metrics in the existing works on video frame interpolation and video deblurring are: PSNR, SSIM and LPIPS. Exactly in that order. 

The main purpose of creating my rankings is to look for the best perceptually-oriented model for practical applications - hence the primary metric in my rankings will be the most common perceptual image quality metric in scientific papers: LPIPS. 

At the time of writing these words, in October 2023, in relation to VFI, I have only found another perceptual image quality metric - DISTS in one paper: [![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) and also in one paper I found a bespoke VFI metric - FloLPIPS [[arXiv]](https://arxiv.org/abs/2303.09508). Unfortunately, both of these papers omit to evaluate the best performing models based on the LPIPS metric. If, in the future, some researcher will evaluate LPIPS top-performing models using alternative, better perceptual metrics, I would of course be happy to add rankings based on those metrics.

I would like to use only one metric - LPIPS. Unfortunately still many of the best VFI and video deblurring methods are only evaluated using PSNR or PSNR and SSIM. For this reason, I will additionally present rankings based on PSNR, which will show the models that can, after perceptually-oriented training, be the best for practical applications, as well as providing a source of knowledge for building even better practical models in the future.

I have decided to completely abandon rankings based on the SSIM metric. Below are the main reasons for this decision, ranked from the most important to the less important.

- The main reason is the following quote, which I found in a paper by researchers at Adobe Research: [^28]. In the quote they refer to a paper by researchers at NVIDIA: [[arXiv]](https://arxiv.org/abs/2006.13846).
  > We limit the evaluation herein to the PSNR metric since SSIM [57] is subject to unexpected and unintuitive results [39].  

- The second reason is, more and more papers are appearing where PSNR scores are given, but without SSIM: [^42] and [![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) A model from such a paper appearing only in the PSNR-based ranking and at the same time not appearing in the SSIM-based ranking may give the misleading impression that the SSIM score is so poor that it does not exceed the ranking eligibility threshold, while there is simply no SSIM score in a paper.

- The third reason is, that often the SSIM scores of individual models are very close to each other or identical. This is the case in the SNU-FILM Easy test, as shown in Table 3: [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html), where as many as 6 models achieve the same score of 0.991 and as many as 5 models achieve the same score of 0.990. In the same test, PSNR makes it easier to determine the order of the ranking, with the same number of significant digits.

- The fourth reason is that PSNR-based rankings are only ancillary when a model does not have an LPIPS score. For this reason, SSIM rankings do not add value to my repository and only reduce its readability. 

- The fifth reason is that I want to encourage researchers who want to use only two metrics in their paper to use LPIPS and PSNR instead of PSNR and SSIM.

- The sixth reason is that the time saved by dropping the SSIM-based rankings will allow me to add new rankings based on other test data, which will be more useful and valuable.

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Appendix 4: List of all research papers from the above rankings

| Method | Abbr. | Paper | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br />(Alt link) | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; |
|:---:|:---:|:---:|:---:|:---:|
| BiM-VFI | - | BiM-VFI: Bidirectional Motion Field-Guided Frame Interpolation for Video with Non-uniform Motions | [![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2412.11365) | [![GitHub Stars](https://img.shields.io/github/stars/KAIST-VICLab/BiM-VFI)](https://github.com/KAIST-VICLab/BiM-VFI) |
| BiT | - | Blur Interpolation Transformer for Real-World Motion from Blur | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhong_Blur_Interpolation_Transformer_for_Real-World_Motion_From_Blur_CVPR_2023_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/BiT)](https://github.com/zzh-tech/BiT) |
| CBBD | - | Frame Interpolation with Consecutive Brownian Bridge Diffusion | [![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3680961)<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2405.05953) | [![GitHub Stars](https://img.shields.io/github/stars/ZonglinL/ConsecutiveBrownianBridge)](https://github.com/ZonglinL/ConsecutiveBrownianBridge) |
| CtxSyn | - | Context-aware Synthesis for Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2018-CVPR-1e407f)](https://openaccess.thecvf.com/content_cvpr_2018/html/Niklaus_Context-Aware_Synthesis_for_CVPR_2018_paper.html) | - |
| DeMFI | - | DeMFI: Deep Joint Deblurring and Multi-Frame Interpolation with Flow-Guided Attentive Correlation and Recursive Boosting | [![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4406_ECCV_2022_paper.php) | [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/DeMFI)](https://github.com/JihyongOh/DeMFI) |
| DvP | - | Dual-view Pyramid Network for Video Frame Interpolation | [![MM](https://img.shields.io/badge/2024-MM-cc1962)](https://dl.acm.org/doi/10.1145/3664647.3681555)<br />[![OpenReview](https://img.shields.io/badge/OpenReview-8c1b13)](https://openreview.net/forum?id=S6fd7X47Ra) | - |
| EDEN | - | EDEN: Enhanced Diffusion for High-quality Large-motion Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2503.15831) | [![GitHub Stars](https://img.shields.io/github/stars/bbldCVer/EDEN)](https://github.com/bbldCVer/EDEN) |
| EDSC | - | Multiple Video Frame Interpolation via Enhanced Deformable Separable Convolution | [![TPAMI](https://img.shields.io/badge/2021-TPAMI-fefd02)](https://ieeexplore.ieee.org/document/9501506)<br />[![arXiv](https://img.shields.io/badge/2020-arXiv-b31b1b)](https://arxiv.org/abs/2006.08070) | [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch)](https://github.com/Xianhang/EDSC-pytorch) |
| EMA-VFI | - | Extracting Motion and Appearance via Inter-Frame Attention for Efficient Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Extracting_Motion_and_Appearance_via_Inter-Frame_Attention_for_Efficient_Video_CVPR_2023_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI)](https://github.com/MCG-NJU/EMA-VFI) |
| FILM | - | FILM: Frame Interpolation for Large Motion | [![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) | [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation)](https://github.com/google-research/frame-interpolation) |
| GIMM-VFI | - | Generalizable Implicit Motion Modeling for Video Frame Interpolation | [![NeurIPS](https://img.shields.io/badge/2024-NeurIPS-68448a)](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7495fa446f10e9edef6e47b2d327596e-Abstract-Conference.html)<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.08680) | [![GitHub Stars](https://img.shields.io/github/stars/GSeanCDAT/GIMM-VFI)](https://github.com/GSeanCDAT/GIMM-VFI) |
| HFD | - | Hierarchical Flow Diffusion for Efficient Frame Interpolation | [![CVPR](https://img.shields.io/badge/2025-CVPR-1e407f)](https://arxiv.org/abs/2504.00380) | - |
| InterpAny-Clearer | IA-Clearer | Clearer Frames, Anytime: Resolving Velocity Ambiguity in Video Frame Interpolation | [![ECCV](https://img.shields.io/badge/2024-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/4908_ECCV_2024_paper.php) | [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/InterpAny-Clearer)](https://github.com/zzh-tech/InterpAny-Clearer) |
| M2M | - | Many-to-many Splatting for Efficient Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Hu_Many-to-Many_Splatting_for_Efficient_Video_Frame_Interpolation_CVPR_2022_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/feinanshan/M2M_VFI)](https://github.com/feinanshan/M2M_VFI) |
| MoMo | - | Disentangled Motion Modeling for Video Frame Interpolation | [![AAAI](https://img.shields.io/badge/2025-AAAI-fddfa0)](https://ojs.aaai.org/index.php/AAAI/article/view/32486)<br />[![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.17256) | [![GitHub Stars](https://img.shields.io/github/stars/JHLew/MoMo)](https://github.com/JHLew/MoMo) |
| PerVFI | - | Perception-Oriented Video Frame Interpolation via Asymmetric Blending | [![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Perception-Oriented_Video_Frame_Interpolation_via_Asymmetric_Blending_CVPR_2024_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/mulns/PerVFI)](https://github.com/mulns/PerVFI) |
| PRF | - | Video Frame Interpolation and Enhancement via Pyramid Recurrent Framework | [![TIP](https://img.shields.io/badge/2020-TIP-dba2a7)](https://ieeexplore.ieee.org/document/9257179) | [![GitHub Stars](https://img.shields.io/github/stars/laomao0/BIN)](https://github.com/laomao0/BIN) |
| SepConv | - | Video Frame Interpolation via Adaptive Separable Convolution | [![ICCV](https://img.shields.io/badge/2017-ICCV-fcb900)](https://openaccess.thecvf.com/content_iccv_2017/html/Niklaus_Video_Frame_Interpolation_ICCV_2017_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/sepconv-slomo)](https://github.com/sniklaus/sepconv-slomo) |
| UPR-Net | - | A Unified Pyramid Recurrent Network for Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_A_Unified_Pyramid_Recurrent_Network_for_Video_Frame_Interpolation_CVPR_2023_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net)](https://github.com/srcn-ivl/UPR-Net) |
| UGFI | - | Frame Interpolation Transformer and Uncertainty Guidance | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html) | - |
| XVFI | - | XVFI: eXtreme Video Frame Interpolation | [![ICCV](https://img.shields.io/badge/2021-ICCV-fcb900)](https://openaccess.thecvf.com/content/ICCV2021/html/Sim_XVFI_eXtreme_Video_Frame_Interpolation_ICCV_2021_paper.html) | [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/XVFI)](https://github.com/JihyongOh/XVFI) |

| Method | Paper | &nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;&nbsp; |
|:---:|:---:|:---:|
| ABME |  |  |
| AdaFNIO |  |  |
| AMT |  |  |
| CDFI |  |  |
| DBVI |  |  |
| DQBC |  |  |
| DRVI |  |  |
| EAFI | Error-Aware Spatial Ensembles for Video Frame Interpolation | [![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2207.12305) |
| EBME |  |  |
| EDC | Enhancing Deformable Convolution based Video Frame Interpolation with Coarse-to-fine 3D CNN | [![ICIP](https://img.shields.io/badge/2022-ICIP-a6539b)](https://ieeexplore.ieee.org/document/9897929) |
| EDENVFI |  |  |
| FGDCN |  |  |
| FLAVR | FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation | [![WACV](https://img.shields.io/badge/2023-WACV-2e0094)](https://openaccess.thecvf.com/content/WACV2023/html/Kalluri_FLAVR_Flow-Agnostic_Video_Representations_for_Fast_Frame_Interpolation_WACV_2023_paper.html) |
| HiFI | High-Resolution Frame Interpolation with Patch-based Cascaded Diffusion | [![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2410.11838) |
| HRFFM | Video Frame Interpolation with Region-Distinguishable Priors from SAM | [![arXiv](https://img.shields.io/badge/2023-arXiv-b31b1b)](https://arxiv.org/abs/2312.15868) |
| H-VFI |  |  |
| IFRNet | IFRNet: Intermediate Feature Refine Network for Efficient Frame Interpolation | [![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Kong_IFRNet_Intermediate_Feature_Refine_Network_for_Efficient_Frame_Interpolation_CVPR_2022_paper.html) |
| IQ-VFI | IQ-VFI: Implicit Quadratic Motion Estimation for Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2024-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2024/html/Hu_IQ-VFI_Implicit_Quadratic_Motion_Estimation_for_Video_Frame_Interpolation_CVPR_2024_paper.html) |
| JNMR |  |  |
| LADDER | LADDER: An Efficient Framework for Video Frame Interpolation | [![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2404.11108) |
| MA-GCSPA | Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) |
| NCM |  |  |
| ProBoost-Net | Progressive Motion Boosting for Video Frame Interpolation | [![TMM](https://img.shields.io/badge/2022-TMM-f6d6bd)](https://ieeexplore.ieee.org/document/10003662) |
| RIFE | Real-Time Intermediate Flow Estimation for Video Frame Interpolation | [![ECCV](https://img.shields.io/badge/2022-ECCV-67cd84)](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/95_ECCV_2022_paper.php) |
| RN-VFI | Range-nullspace Video Frame Interpolation with Focalized Motion Estimation | [![CVPR](https://img.shields.io/badge/2023-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html) |
| SoftSplat | Softmax Splatting for Video Frame Interpolation | [![CVPR](https://img.shields.io/badge/2020-CVPR-1e407f)](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) |
| SSR | Video Frame Interpolation with Many-to-many Splatting and Spatial Selective Refinement | [![TPAMI](https://img.shields.io/badge/2024-TPAMI-fefd02)](https://ieeexplore.ieee.org/document/10294102) |
| ST-MFNet |  |  |
| Swin-VFI | Video Frame Interpolation for Polarization via Swin-Transformer | [![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2406.11371) |
| TDPNet | Textural Detail Preservation Network for Video Frame Interpolation | [![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) |
| TTVFI |  |  |
| VFIformer | Video Frame Interpolation with Transformer | [![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Lu_Video_Frame_Interpolation_With_Transformer_CVPR_2022_paper.html) |
| VFIFT | Video Frame Interpolation with Flow Transformer | [![MM](https://img.shields.io/badge/2023-MM-cc1962)](https://dl.acm.org/doi/10.1145/3581783.3612440) |
| VFIMamba | VFIMamba: Video Frame Interpolation with State Space Models | [![arXiv](https://img.shields.io/badge/2024-arXiv-b31b1b)](https://arxiv.org/abs/2407.02315) |
| VFIT | Video Frame Interpolation Transformer | [![CVPR](https://img.shields.io/badge/2022-CVPR-1e407f)](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) |
| VRT | VRT: A Video Restoration Transformer | [![arXiv](https://img.shields.io/badge/2022-arXiv-b31b1b)](https://arxiv.org/abs/2201.12288) |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

[^1]: JNMR: Joint Non-linear Motion Regression for Video Frame Interpolation [[TIP 2023]](https://ieeexplore.ieee.org/document/10255610) [[arXiv]](https://arxiv.org/abs/2206.04231)
[^2]: Video Frame Interpolation Transformer [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2111.13817)
[^3]: Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2203.10291)
[^4]: TTVFI: Learning Trajectory-Aware Transformer for Video Frame Interpolation [[TIP 2023]](https://ieeexplore.ieee.org/document/10215337) [[arXiv]](https://arxiv.org/abs/2207.09048)


[^7]: ST-MFNet: A Spatio-Temporal Multi-Flow Network for Frame Interpolation [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Danier_ST-MFNet_A_Spatio-Temporal_Multi-Flow_Network_for_Frame_Interpolation_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2111.15483)
[^8]: Error-Aware Spatial Ensembles for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.12305)
[^9]: FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation [[WACV 2023]](https://openaccess.thecvf.com/content/WACV2023/html/Kalluri_FLAVR_Flow-Agnostic_Video_Representations_for_Fast_Frame_Interpolation_WACV_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2012.08512)
[^10]: IFRNet: Intermediate Feature Refine Network for Efficient Frame Interpolation [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Kong_IFRNet_Intermediate_Feature_Refine_Network_for_Efficient_Frame_Interpolation_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2205.14620)
[^11]: Enhanced Bi-directional Motion Estimation for Video Frame Interpolation [[WACV 2023]](https://openaccess.thecvf.com/content/WACV2023/html/Jin_Enhanced_Bi-Directional_Motion_Estimation_for_Video_Frame_Interpolation_WACV_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2206.08572)
[^12]: Real-Time Intermediate Flow Estimation for Video Frame Interpolation [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/95_ECCV_2022_paper.php) [[arXiv]](https://arxiv.org/abs/2011.06294)
[^13]: Asymmetric Bilateral Motion Estimation for Video Frame Interpolation [[ICCV 2021]](https://openaccess.thecvf.com/content/ICCV2021/html/Park_Asymmetric_Bilateral_Motion_Estimation_for_Video_Frame_Interpolation_ICCV_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2108.06815)
[^14]: Enhancing Deformable Convolution based Video Frame Interpolation with Coarse-to-fine 3D CNN [[ICIP 2022]](https://ieeexplore.ieee.org/document/9897929) [[arXiv]](https://arxiv.org/abs/2202.07731)
[^15]: Softmax Splatting for Video Frame Interpolation [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) [[arXiv]](https://arxiv.org/abs/2003.05534)

[^17]: Deep Bayesian Video Frame Interpolation [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/1287_ECCV_2022_paper.php)
[^18]: A Unified Pyramid Recurrent Network for Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_A_Unified_Pyramid_Recurrent_Network_for_Video_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2211.03456)
[^19]: AdaFNIO: Adaptive Fourier Neural Interpolation Operator for video frame interpolation [[arXiv]](https://arxiv.org/abs/2211.10791)
[^20]: H-VFI: Hierarchical Frame Interpolation for Videos with Large Motions [[arXiv]](https://arxiv.org/abs/2211.11309)
[^21]: Flow Guidance Deformable Compensation Network for Video Frame Interpolation [[TMM 2023]](https://ieeexplore.ieee.org/document/10164197) [[arXiv]](https://arxiv.org/abs/2211.12117)
[^22]: Extracting Motion and Appearance via Inter-Frame Attention for Efficient Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhang_Extracting_Motion_and_Appearance_via_Inter-Frame_Attention_for_Efficient_Video_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2303.00440)
[^23]: AdaPool: Exponential Adaptive Pooling for Information-Retaining Downsampling [[TIP 2022]](https://ieeexplore.ieee.org/document/9982650) [[arXiv]](https://arxiv.org/abs/2111.00772)
[^24]: CDFI: Compression-Driven Network Design for Frame Interpolation [[CVPR 2021]](https://openaccess.thecvf.com/content/CVPR2021/html/Ding_CDFI_Compression-Driven_Network_Design_for_Frame_Interpolation_CVPR_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2103.10559)
[^25]: Multiple Video Frame Interpolation via Enhanced Deformable Separable Convolution [[TPAMI 2021]](https://ieeexplore.ieee.org/document/9501506) [[arXiv]](https://arxiv.org/abs/2006.08070)
[^26]: DRVI: Dual Refinement for Video Interpolation [[Access 2021]](https://ieeexplore.ieee.org/document/9513293)

[^28]: Revisiting Adaptive Convolutions for Video Frame Interpolation [[WACV 2021]](https://openaccess.thecvf.com/content/WACV2021/html/Niklaus_Revisiting_Adaptive_Convolutions_for_Video_Frame_Interpolation_WACV_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2011.01280)
[^29]: Locally Adaptive Structure and Texture Similarity for Image Quality Assessment [[MM 2021]](https://dl.acm.org/doi/10.1145/3474085.3475419) [[arXiv]](https://arxiv.org/abs/2110.08521)
[^30]: The Unreasonable Effectiveness of Deep Features as a Perceptual Metric [[CVPR 2018]](https://openaccess.thecvf.com/content_cvpr_2018/html/Zhang_The_Unreasonable_Effectiveness_CVPR_2018_paper.html) [[arXiv]](https://arxiv.org/abs/1801.03924)
[^31]: AMT: All-Pairs Multi-Field Transforms for Efficient Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Li_AMT_All-Pairs_Multi-Field_Transforms_for_Efficient_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2304.09790)
[^32]: Neighbor Correspondence Matching for Flow-based Video Frame Synthesis [[MM 2022]](https://dl.acm.org/doi/10.1145/3503161.3548163) [[arXiv]](https://arxiv.org/abs/2207.06763)
[^33]: Blur Interpolation Transformer for Real-World Motion from Blur [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhong_Blur_Interpolation_Transformer_for_Real-World_Motion_From_Blur_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2211.11423)
[^34]: DeMFI: Deep Joint Deblurring and Multi-Frame Interpolation with Flow-Guided Attentive Correlation and Recursive Boosting [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4406_ECCV_2022_paper.php) [[arXiv]](https://arxiv.org/abs/2111.09985)
[^35]: Blurry Video Frame Interpolation [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/html/Shen_Blurry_Video_Frame_Interpolation_CVPR_2020_paper.html) [[arXiv]](https://arxiv.org/abs/2002.12259)
[^36]: Video Frame Interpolation with Densely Queried Bilateral Correlation [[IJCAI 2023]](https://www.ijcai.org/proceedings/2023/198) [[arXiv]](https://arxiv.org/abs/2304.13596)

[^38]: Video Frame Interpolation and Enhancement via Pyramid Recurrent Framework [[TIP 2020]](https://ieeexplore.ieee.org/document/9257179)



[^42]: Efficient Convolution and Transformer-Based Network for Video Frame Interpolation [[ICIP 2023]](https://ieeexplore.ieee.org/document/10222296) [[arXiv]](https://arxiv.org/abs/2307.06443)
