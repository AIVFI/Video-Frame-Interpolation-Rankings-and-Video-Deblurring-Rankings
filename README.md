# <p align=center>Video Frame Interpolation Rankings<br />and Video Deblurring Rankings</p>

**Announcement on 15 September 2023**: From Monday I will gradually change the layout of tables. The most important change is the introduction of badges which, when clicked on, will direct to websites with published papers for the models included in the rankings. This will allow me to completely eliminate the footnotes, which in my opinion are a nuisance when browsing the rankings. Also, the GitHub badges will direct to repository websites. The new GitHub badges will have the GitHub logo. In the tables, there will be new information about the models: Input Frames and Training dataset. As these changes are not currently my priority, the old and new layouts of the tables will appear simultaneously for some time. However, all new models added to the rankings will include the changes described above. The new layout of tables can already be checked and tested today in my second repository: [Monocular Video Depth Estimation Rankings and Light Field Video Reconstruction from Monocular Video Rankings](https://github.com/AIVFI/Monocular-Video-Depth-Estimation-Rankings-and-Light-Field-Video-Reconstruction-from-MV-Rankings) If anyone has any comments or suggestions in this regard, please let me know.

--------------------
Gradually I intend to add new rankings, but my priority is to keep the existing ones up to date. Below is a list of <ins>**4 upcoming updates**</ins> that <ins>**I intend to add**</ins> to keep the existing rankings up to date:
1. Add enhanced models: [[arXiv]](https://arxiv.org/abs/2306.13933)
1. Add new model: [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html)
1. Add new model: [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html)
1. Add new model: VFIFT [[arXiv]](https://arxiv.org/abs/2307.16144)

An introduction to the rankings is in the development process....

--------------------
Researchers! Please train at least one of your models on **perceptual loss**. I have made a special column in my rankings dedicated specifically to such models. Why models trained on perceptual loss? This is best summarised by the following quote [^15]:

> "the model trained using color loss 𝓛<sub>*Lap*</sub> performs best in
terms of PSNR and SSIM whereas **the one trained using perceptual
loss 𝓛<sub>*F*</sub> performs best in terms of LPIPS**. We further
note that the 𝓛<sub>*F*</sub>-trained model **better recovers fine details in
challenging cases, making it preferable in practice**."

It can be seen from the results of two **video frame interpolation models** from the quote above on the  Vimeo-90K triplet test set [^15]:

| Model | PSNR ↑ | SSIM ↑ | LPIPS ↓ |
|:----|:----:|:----:|:----:|
| SoftSplat - 𝓛<sub>*Lap*</sub> | <ins>**36.10dB**</ins> | <ins>**0.970**</ins> | 0.021 |
| SoftSplat - 𝓛<sub>*F*</sub> | 35.48dB | 0.964 | <ins>**0.013**</ins> |

Sometimes even almost 3dB better PSNR result does not guarantee better LPIPS result, as shown by the results of two different video frame interpolation methods on the Vimeo-90K septuplet test set [^27]:

| Model | PSNR ↑ | SSIM ↑ | LPIPS ↓ |
|:----|:----:|:----:|:----:|
| VFIT-B | <ins>**36.963dB**</ins> | <ins>**0.9649**</ins> | 0.0304 |
| RIFE | 34.048dB | 0.9449 | <ins>**0.0233**</ins> |

LPIPS [^30] is a metric that reflects human perception much better than PSNR or SSIM, which is also evident from the results presented in the paper of the competitive perceptual metric [^29]:

| IQA<br />Model | BAPPS database<br />Frame interpolation<br />2AFC score ↑ | BAPPS database<br />Video deblurring<br />2AFC score ↑ | Ding20 database<br />Deblurring<br />2AFC score ↑ |
|:----|:----:|:----:|:----:|
| Human | 0.686 | 0.671 | 0.843 |
| LPIPS | 0.630 | 0.605 | 0.788 |
| PSNR | 0.543 | 0.590 | 0.518 |
| SSIM | 0.548 | 0.583 | 0.575 |

## <p align=center>List of Rankings</p>
<p align=center>Each ranking includes only the best model for one method.</p>  
<p align=center>The rankings exclude all event-based models.</p>

### Joint Video Deblurring and Frame Interpolation Rankings
1. :crown: **RBI with real motion blur:heavy_check_mark:: LPIPS:heart_eyes:** (no data)  
*This will be the King of all rankings. We look forward to ambitious researchers.*
1. [**RBI with real motion blur:heavy_check_mark:: PSNR:disappointed:>=28.5dB**](#rbi-with-real-motion-blurheavy_check_mark-psnrdisappointed285db)
1. **Adobe240 (640×352) with synthetic motion blur:bangbang:: LPIPS:heart_eyes:** (no data)  
1. [**Adobe240 (640×352) with synthetic motion blur:bangbang:: PSNR:disappointed:>=33.3dB**](#adobe240-640352-with-synthetic-motion-blurbangbang-psnrdisappointed333db)
1. **Adobe240 (5:8) with synthetic motion blur:bangbang:: LPIPS:heart_eyes:** (no data)
1. [**Adobe240 (5:8) with synthetic motion blur:bangbang:: PSNR:disappointed:>=25dB**](#adobe240-58-with-synthetic-motion-blurbangbang-psnrdisappointed25db)
### Video Deblurring Rankings
- (to do)
### Video Frame Interpolation Rankings
1. [**Vimeo-90K triplet: LPIPS:heart_eyes:(SqueezeNet)<=0.014**](#vimeo-90k-triplet-lpipsheart_eyessqueezenet0014)
1. [**Vimeo-90K triplet: LPIPS:heart_eyes:<=0.016**](#vimeo-90k-triplet-lpipsheart_eyes0016)
1. [**Vimeo-90K triplet: PSNR:disappointed:>=36dB**](#vimeo-90k-triplet-psnrdisappointed36db)
1. [**Vimeo-90K septuplet: LPIPS:heart_eyes:<=0.032**](#vimeo-90k-septuplet-lpipsheart_eyes0032)
1. [**Vimeo-90K septuplet: PSNR:disappointed:>=36dB**](#vimeo-90k-septuplet-psnrdisappointed36db)
### Appendices
- **Appendix 1: Rules for qualifying models for the rankings** (to do)
- [**Appendix 2: Metrics selection for the rankings**](#appendix-2-metrics-selection-for-the-rankings)

--------------------

## RBI with real motion blur:heavy_check_mark:: PSNR:disappointed:>=28.5dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | Pre-BiT++ |  **31.32dB** [^33] | November 2022 [^33] | [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/BiT?logo=GitHub&label=Stars)](https://github.com/zzh-tech/BiT) | [<img alt="Request" width="40px" src="cat.png">](https://github.com/zzh-tech/BiT/issues/5) | - |
| 2 | DeMFI-Net<sub>*rb*</sub>(5,3) |  **29.03dB** [^33] | November 2021 [^34] | [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/DeMFI?logo=GitHub&label=Stars)](https://github.com/JihyongOh/DeMFI) | - | - |
| 3 | PRF<sub>4</sub> -*Large* |  **28.55dB** [^33] | February 2020 [^35] | [![GitHub Stars](https://img.shields.io/github/stars/laomao0/BIN?logo=GitHub&label=Stars)](https://github.com/laomao0/BIN) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Adobe240 (640×352) with synthetic motion blur:bangbang:: PSNR:disappointed:>=33.3dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | BiT++ |  **34.97dB** [^33] | November 2022 [^33] | [![GitHub Stars](https://img.shields.io/github/stars/zzh-tech/BiT?logo=GitHub&label=Stars)](https://github.com/zzh-tech/BiT) | [<img alt="Request" width="40px" src="cat.png">](https://github.com/zzh-tech/BiT/issues/5) | - |
| 2 | DeMFI-Net<sub>*rb*</sub>(5,3) |  **34.34dB** [^34] | November 2021 [^34] | [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/DeMFI?logo=GitHub&label=Stars)](https://github.com/JihyongOh/DeMFI) | - | - |
| 3 | ALANET |  **33.34dB** [^37] | August 2020 [^37] | [![GitHub Stars](https://img.shields.io/github/stars/agupt013/ALANET?logo=GitHub&label=Stars)](https://github.com/agupt013/ALANET) | - | - |
| 4 | PRF<sub>4</sub> -*Large* |  **33.32dB** [^38] | February 2020 [^35] | [![GitHub Stars](https://img.shields.io/github/stars/laomao0/BIN?logo=GitHub&label=Stars)](https://github.com/laomao0/BIN) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Adobe240 (5:8) with synthetic motion blur:bangbang:: PSNR:disappointed:>=25dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | VIDUE |  **28.74dB** [^39] | March 2023 [^39] | [![GitHub Stars](https://img.shields.io/github/stars/shangwei5/VIDUE?logo=GitHub&label=Stars)](https://github.com/shangwei5/VIDUE) | - | - |
| 2 | FLAVR |  **27.23dB** [^39] | December 2020 [^9] | [![GitHub Stars](https://img.shields.io/github/stars/tarun005/FLAVR?logo=GitHub&label=Stars)](https://github.com/tarun005/FLAVR) | - | - |
| 3 | UTI-VFI |  **26.69dB** [^39] | December 2020 [^40] | [![GitHub Stars](https://img.shields.io/github/stars/yjzhang96/UTI-VFI?logo=GitHub&label=Stars)](https://github.com/yjzhang96/UTI-VFI) | - | - |
| 4 | DeMFI |  **25.71dB** [^39] | November 2021 [^34] | [![GitHub Stars](https://img.shields.io/github/stars/JihyongOh/DeMFI?logo=GitHub&label=Stars)](https://github.com/JihyongOh/DeMFI) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: LPIPS:heart_eyes:(SqueezeNet)<=0.014
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | CDFI w/ adaP/U |  **0.008** [^23] | March 2021 [^24] | [![GitHub Stars](https://img.shields.io/github/stars/tding1/CDFI?logo=GitHub&label=Stars)](https://github.com/tding1/CDFI) | - | - |
| 2 | EDSC_s-𝓛<sub>*F*</sub> |  **0.010** [^24] | June 2020 [^25] | [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch?logo=GitHub&label=Stars)](https://github.com/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |
| 3 | DRVI |  **0.013** [^26] | August 2021 [^26] | - | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: LPIPS:heart_eyes:<=0.016
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | EAFI-𝓛<sub>*ecp*</sub> |  **0.012** [^8] | July 2022 [^8] | - | - | - |
| 2 | SoftSplat - 𝓛<sub>*F*</sub> |  **0.013** [^15] | March 2020 [^15] | [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting?logo=GitHub&label=Stars)](https://github.com/sniklaus/softmax-splatting) | - | - |
| 3 | EDSC_s-𝓛<sub>*F*</sub> |  **0.016** [^25] | June 2020 [^25] | [![GitHub Stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch?logo=GitHub&label=Stars)](https://github.com/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K triplet: PSNR:disappointed:>=36dB

| Rank | &nbsp;&nbsp;&nbsp;&nbsp;Model&nbsp;&nbsp;&nbsp;&nbsp; | &nbsp;&nbsp;&nbsp;PSNR&nbsp;↑&nbsp;&nbsp;&nbsp;<br />{Input&nbsp;fr.} | Originally<br />announced<br />or Training<br />dataset | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | MA-GCSPA triplet-trained |  **36.76dB** [^3] | March 2022 [^3] | [![GitHub Stars](https://img.shields.io/github/stars/redrock303/CVPR23-MA-GCSPA?logo=GitHub&label=Stars)](https://github.com/redrock303/CVPR23-MA-GCSPA) | - | - |
| 2 | EMA-VFI |  **36.64dB** [^22] | March 2023 [^22] | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI?logo=GitHub&label=Stars)](https://github.com/MCG-NJU/EMA-VFI) | - | - |
| 3 | DQBC-Aug |  **36.57dB** [^36] | April 2023 [^36] | [![GitHub Stars](https://img.shields.io/github/stars/kinoud/DQBC?logo=GitHub&label=Stars)](https://github.com/kinoud/DQBC) | - | - |
| 4 | TTVFI |  **36.54dB** [^4] | July 2022 [^4] | [![GitHub Stars](https://img.shields.io/github/stars/ChengxuLiu/TTVFI?logo=GitHub&label=Stars)](https://github.com/ChengxuLiu/TTVFI) | - | - |
| 5 | AMT-G |  **36.53dB** [^31] | April 2023 [^31] | [![GitHub Stars](https://img.shields.io/github/stars/MCG-NKU/AMT?logo=GitHub&label=Stars)](https://github.com/MCG-NKU/AMT) | - | - |
| 6-7 | AdaFNIO |  **36.50dB** [^19] | November 2022 [^19] | [![GitHub Stars](https://img.shields.io/github/stars/IDEAS-Lab-Purdue/AdaFNIO?logo=GitHub&label=Stars)](https://github.com/IDEAS-Lab-Purdue/AdaFNIO) | - | - |
| 6-7 | VFIformer |  **36.50dB** [^6] | May 2022 [^6] | [![GitHub Stars](https://img.shields.io/github/stars/dvlab-research/VFIformer?logo=GitHub&label=Stars)](https://github.com/dvlab-research/VFIformer) | - | - |
| 8 | FGDCN-L |  **36.46dB** [^21] | November 2022 [^21] | [![GitHub Stars](https://img.shields.io/github/stars/lpcccc-cv/FGDCN?logo=GitHub&label=Stars)](https://github.com/lpcccc-cv/FGDCN) | - | - |
| 9 | UPR-Net LARGE |  **36.42dB** [^18] | November 2022 [^18] | [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net?logo=GitHub&label=Stars)](https://github.com/srcn-ivl/UPR-Net) | - | - |
| 10 | EAFI-𝓛<sub>*ecc*</sub> |  **36.38dB** [^8] | July 2022 [^8] | - | - | - |
| 11 | H-VFI-Large |  **36.37dB** [^20] | November 2022 [^20] | - | - | - |
| 12 | SoftSplat - 𝓛<sub>*Lap*</sub> with ensemble |  **36.28dB** [^28] | March 2020 [^15] | [![GitHub Stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting?logo=GitHub&label=Stars)](https://github.com/sniklaus/softmax-splatting) | - | - |
| 13 | NCM-Large |  **36.22dB** [^32] | July 2022 [^32] | - | - | - |
| 14 | IFRNet large |  **36.20dB** [^10] | May 2022 [^10] | [![GitHub Stars](https://img.shields.io/github/stars/ltkong218/IFRNet?logo=GitHub&label=Stars)](https://github.com/ltkong218/IFRNet) | - | - |
| 15-16 | EBME-H* |  **36.19dB** [^11] | June 2022 [^11] | [![GitHub Stars](https://img.shields.io/github/stars/srcn-ivl/EBME?logo=GitHub&label=Stars)](https://github.com/srcn-ivl/EBME) | - | - |
| 15-16 | RIFE-Large |  **36.19dB** [^12] | November 2020 [^12] | [![GitHub Stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE?logo=GitHub&label=Stars)](https://github.com/megvii-research/ECCV2022-RIFE) | [RIFE v4.7](https://github.com/hzwer/Practical-RIFE#model-list) | [![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/AmusementClub/vs-mlrt)<br />[![GitHub Stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt?logo=GitHub&label=Stars)](https://github.com/AmusementClub/vs-mlrt)<br />[![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/HolyWu/vs-rife)<br />[![GitHub Stars](https://img.shields.io/github/stars/HolyWu/vs-rife?logo=GitHub&label=Stars)](https://github.com/HolyWu/vs-rife)<br />[![ncnn](https://img.shields.io/badge/ncnn-0052d9)](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[![GitHub Stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan?logo=GitHub&label=Stars)](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[![ncnn](https://img.shields.io/badge/ncnn-0052d9)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />[![GitHub Stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan?logo=GitHub&label=Stars)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 17 | ABME |  **36.18dB** [^13] | August 2021 [^13] | [![GitHub Stars](https://img.shields.io/github/stars/JunHeum/ABME?logo=GitHub&label=Stars)](https://github.com/JunHeum/ABME) | - | - |
| 18 | TDPNet<sub>*nv*</sub> w/o MRTM<br />[![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) | **36.069** {2}<br />[![Access](https://img.shields.io/badge/2023-Access-00b5e2)](https://ieeexplore.ieee.org/document/10182248) | Vimeo-90K triplet | - | - | - |
| 19 | FILM-𝓛<sub>1</sub> |  **36.06dB** [^16] | February 2022 [^16] | [![GitHub Stars](https://img.shields.io/github/stars/google-research/frame-interpolation?logo=GitHub&label=Stars)](https://github.com/google-research/frame-interpolation) | [FILM-𝓛<sub>*S*</sub>](https://github.com/google-research/frame-interpolation#pre-trained-models) | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K septuplet: LPIPS:heart_eyes:<=0.032
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | RIFE |  **0.0233** [^27] | November 2020 [^12] | [![GitHub Stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE?logo=GitHub&label=Stars)](https://github.com/megvii-research/ECCV2022-RIFE) | [RIFE v4.7](https://github.com/hzwer/Practical-RIFE#model-list) | [![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/AmusementClub/vs-mlrt)<br />[![GitHub Stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt?logo=GitHub&label=Stars)](https://github.com/AmusementClub/vs-mlrt)<br />[![TensorRT](https://img.shields.io/badge/TensorRT-77b900)](https://github.com/HolyWu/vs-rife)<br />[![GitHub Stars](https://img.shields.io/github/stars/HolyWu/vs-rife?logo=GitHub&label=Stars)](https://github.com/HolyWu/vs-rife)<br />[![ncnn](https://img.shields.io/badge/ncnn-0052d9)](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[![GitHub Stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan?logo=GitHub&label=Stars)](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[![ncnn](https://img.shields.io/badge/ncnn-0052d9)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />[![GitHub Stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan?logo=GitHub&label=Stars)](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 2 | IFRNet |  **0.0274** [^27] | May 2022 [^10] | [![GitHub Stars](https://img.shields.io/github/stars/ltkong218/IFRNet?logo=GitHub&label=Stars)](https://github.com/ltkong218/IFRNet) | - | - |
| 3 | VFIT-B | **0.0304** [^27] | November 2021 [^2] | [![GitHub Stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer?logo=GitHub&label=Stars)](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 4 | ABME |  **0.0309** [^27] | August 2021 [^13] | [![GitHub Stars](https://img.shields.io/github/stars/JunHeum/ABME?logo=GitHub&label=Stars)](https://github.com/JunHeum/ABME) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Vimeo-90K septuplet: PSNR:disappointed:>=36dB

| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />&nbsp;&nbsp;repository&nbsp;&nbsp; | Practical<br />model | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | JNMR | **37.09dB** [^1] | June 2022 [^1] | [![GitHub Stars](https://img.shields.io/github/stars/ruhig6/JNMR?logo=GitHub&label=Stars)](https://github.com/ruhig6/JNMR) | - | - |
| 2 | VFIT-B | **36.96dB** [^2] | November 2021 [^2] | [![GitHub Stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer?logo=GitHub&label=Stars)](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 3 | VRT |  **36.53dB** [^5] | June 2022 (VFI) [^5] | [![GitHub Stars](https://img.shields.io/github/stars/JingyunLiang/VRT?logo=GitHub&label=Stars)](https://github.com/JingyunLiang/VRT) | - | - |
| 4 | ST-MFNet | **36.507dB** [^42] | November 2021 [^7] | [![GitHub Stars](https://img.shields.io/github/stars/danielism97/ST-MFNet?logo=GitHub&label=Stars)](https://github.com/danielism97/ST-MFNet) | - | - |
| 5 | MA-GCSPA septuplet-trained |  **36.50dB** [^3] | March 2022 [^3] | [![GitHub Stars](https://img.shields.io/github/stars/redrock303/CVPR23-MA-GCSPA?logo=GitHub&label=Stars)](https://github.com/redrock303/CVPR23-MA-GCSPA) | - | - |
| 6 | EDENVFI PVT(15,15) | **36.387dB** [^42] | July 2023 [^42] | - | - | - |
| 7 | FLAVR |  **36.25dB** [^9] | December 2020 [^9] | [![GitHub Stars](https://img.shields.io/github/stars/tarun005/FLAVR?logo=GitHub&label=Stars)](https://github.com/tarun005/FLAVR) | - | - |
| 8 | DBVI |  **36.17dB** [^17] | October 2022 [^17] | [![GitHub Stars](https://img.shields.io/github/stars/Oceanlib/DBVI?logo=GitHub&label=Stars)](https://github.com/Oceanlib/DBVI) | - | - |
| 9 | EDC | **36.14dB** [^1] | February 2022 [^14] | [![GitHub Stars](https://img.shields.io/github/stars/danielism97/EDC?logo=GitHub&label=Stars)](https://github.com/danielism97/EDC) | - | - |

[![Back to Top](https://img.shields.io/badge/Back_to_Top-555555)](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[![Back to the List of Rankings](https://img.shields.io/badge/Back_to_the_List_of_Rankings-555555)](#list-of-rankings)

## Appendix 2: Metrics selection for the rankings

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

[^1]: JNMR: Joint Non-linear Motion Regression for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2206.04231)
[^2]: Video Frame Interpolation Transformer [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2111.13817)
[^3]: Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2203.10291)
[^4]: TTVFI: Learning Trajectory-Aware Transformer for Video Frame Interpolation [[TIP 2023]](https://ieeexplore.ieee.org/document/10215337) [[arXiv]](https://arxiv.org/abs/2207.09048)
[^5]: VRT: A Video Restoration Transformer [[arXiv]](https://arxiv.org/abs/2201.12288)
[^6]: Video Frame Interpolation with Transformer [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Lu_Video_Frame_Interpolation_With_Transformer_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2205.07230)
[^7]: ST-MFNet: A Spatio-Temporal Multi-Flow Network for Frame Interpolation [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Danier_ST-MFNet_A_Spatio-Temporal_Multi-Flow_Network_for_Frame_Interpolation_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2111.15483)
[^8]: Error-Aware Spatial Ensembles for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.12305)
[^9]: FLAVR: Flow-Agnostic Video Representations for Fast Frame Interpolation [[WACV 2023]](https://openaccess.thecvf.com/content/WACV2023/html/Kalluri_FLAVR_Flow-Agnostic_Video_Representations_for_Fast_Frame_Interpolation_WACV_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2012.08512)
[^10]: IFRNet: Intermediate Feature Refine Network for Efficient Frame Interpolation [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Kong_IFRNet_Intermediate_Feature_Refine_Network_for_Efficient_Frame_Interpolation_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2205.14620)
[^11]: Enhanced Bi-directional Motion Estimation for Video Frame Interpolation [[WACV 2023]](https://openaccess.thecvf.com/content/WACV2023/html/Jin_Enhanced_Bi-Directional_Motion_Estimation_for_Video_Frame_Interpolation_WACV_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2206.08572)
[^12]: Real-Time Intermediate Flow Estimation for Video Frame Interpolation [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/95_ECCV_2022_paper.php) [[arXiv]](https://arxiv.org/abs/2011.06294)
[^13]: Asymmetric Bilateral Motion Estimation for Video Frame Interpolation [[ICCV 2021]](https://openaccess.thecvf.com/content/ICCV2021/html/Park_Asymmetric_Bilateral_Motion_Estimation_for_Video_Frame_Interpolation_ICCV_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2108.06815)
[^14]: Enhancing Deformable Convolution based Video Frame Interpolation with Coarse-to-fine 3D CNN [[ICIP 2022]](https://ieeexplore.ieee.org/document/9897929) [[arXiv]](https://arxiv.org/abs/2202.07731)
[^15]: Softmax Splatting for Video Frame Interpolation [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/html/Niklaus_Softmax_Splatting_for_Video_Frame_Interpolation_CVPR_2020_paper.html) [[arXiv]](https://arxiv.org/abs/2003.05534)
[^16]: FILM: Frame Interpolation for Large Motion [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4614_ECCV_2022_paper.php) [[arXiv]](https://arxiv.org/abs/2202.04901)
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
[^27]: Exploring Discontinuity for Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Lee_Exploring_Discontinuity_for_Video_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2202.07291)
[^28]: Revisiting Adaptive Convolutions for Video Frame Interpolation [[WACV 2021]](https://openaccess.thecvf.com/content/WACV2021/html/Niklaus_Revisiting_Adaptive_Convolutions_for_Video_Frame_Interpolation_WACV_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2011.01280)
[^29]: Locally Adaptive Structure and Texture Similarity for Image Quality Assessment [[MM 2021]](https://dl.acm.org/doi/10.1145/3474085.3475419) [[arXiv]](https://arxiv.org/abs/2110.08521)
[^30]: The Unreasonable Effectiveness of Deep Features as a Perceptual Metric [[CVPR 2018]](https://openaccess.thecvf.com/content_cvpr_2018/html/Zhang_The_Unreasonable_Effectiveness_CVPR_2018_paper.html) [[arXiv]](https://arxiv.org/abs/1801.03924)
[^31]: AMT: All-Pairs Multi-Field Transforms for Efficient Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Li_AMT_All-Pairs_Multi-Field_Transforms_for_Efficient_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2304.09790)
[^32]: Neighbor Correspondence Matching for Flow-based Video Frame Synthesis [[MM 2022]](https://dl.acm.org/doi/10.1145/3503161.3548163) [[arXiv]](https://arxiv.org/abs/2207.06763)
[^33]: Blur Interpolation Transformer for Real-World Motion from Blur [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhong_Blur_Interpolation_Transformer_for_Real-World_Motion_From_Blur_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2211.11423)
[^34]: DeMFI: Deep Joint Deblurring and Multi-Frame Interpolation with Flow-Guided Attentive Correlation and Recursive Boosting [[ECCV 2022]](https://www.ecva.net/papers/eccv_2022/papers_ECCV/html/4406_ECCV_2022_paper.php) [[arXiv]](https://arxiv.org/abs/2111.09985)
[^35]: Blurry Video Frame Interpolation [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/html/Shen_Blurry_Video_Frame_Interpolation_CVPR_2020_paper.html) [[arXiv]](https://arxiv.org/abs/2002.12259)
[^36]: Video Frame Interpolation with Densely Queried Bilateral Correlation [IJCAI 2023] [[arXiv]](https://arxiv.org/abs/2304.13596)
[^37]: ALANET: Adaptive Latent Attention Network for Joint Video Deblurring and Interpolation [[MM 2020]](https://dl.acm.org/doi/10.1145/3394171.3413686) [[arXiv]](https://arxiv.org/abs/2009.01005)
[^38]: Video Frame Interpolation and Enhancement via Pyramid Recurrent Framework [[TIP 2020]](https://ieeexplore.ieee.org/document/9257179)
[^39]: Joint Video Multi-Frame Interpolation and Deblurring under Unknown Exposure Time [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Shang_Joint_Video_Multi-Frame_Interpolation_and_Deblurring_Under_Unknown_Exposure_Time_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2303.15043)
[^40]: Video Frame Interpolation without Temporal Priors [[NeurIPS 2020]](https://proceedings.neurips.cc/paper_files/paper/2020/hash/9a11883317fde3aef2e2432a58c86779-Abstract.html) [[arXiv]](https://arxiv.org/abs/2112.01161)

[^42]: Efficient Convolution and Transformer-Based Network for Video Frame Interpolation [ICIP 2023] [[arXiv]](https://arxiv.org/abs/2307.06443)
