# <p align=center>Video Frame Interpolation Rankings<br />and Video Deblurring Rankings</p>

Gradually I intend to add new rankings, but my priority is to keep the existing ones up to date. Below is a list of <ins>**7 upcoming updates**</ins> that <ins>**I intend to add**</ins> to keep the existing rankings up to date:
1. Modified presentation of enhanced models in the rankings 
1. Enhanced models added: [[arXiv]](https://arxiv.org/abs/2306.13933)
1. Missing enhanced model added: SoftSplat - 𝓛<sub>*Lap*</sub> with ensemble [[WACV 2021]](https://openaccess.thecvf.com/content/WACV2021/html/Niklaus_Revisiting_Adaptive_Convolutions_for_Video_Frame_Interpolation_WACV_2021_paper.html) [[arXiv]](https://arxiv.org/abs/2011.01280)
1. Missing model added: MVFI-Net<sub>*L*</sub> [[ACCV 2022]](https://openaccess.thecvf.com/content/ACCV2022/html/Lin_MVFI-Net_Motion-aware_Video_Frame_Interpolation_Network_ACCV_2022_paper.html)
1. New model added: [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Plack_Frame_Interpolation_Transformer_and_Uncertainty_Guidance_CVPR_2023_paper.html)
1. New model added: [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_Range-Nullspace_Video_Frame_Interpolation_With_Focalized_Motion_Estimation_CVPR_2023_paper.html)
1. New model added: EDENVFI [[arXiv]](https://arxiv.org/abs/2307.06443)

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

The same can also be seen from the results of two **single image deblurring models** on the GoPro test set [^28]:

| Model | PSNR ↑ | SSIM ↑ | LPIPS ↓ | NIQE ↓ | FID ↓ | KID ↓ |
|:----|:----:|:----:|:----:|:----:|:----:|:----:|
| DGD-SA | <ins>**33.20dB**</ins> | <ins>**0.963**</ins> | 0.078 | 4.10 | 8.69 | 0.00706 |
| DGD | 31.19dB | 0.943 | <ins>**0.057**</ins> | <ins>**3.27**</ins> | <ins>**3.50**</ins> | <ins>**0.00077**</ins> |

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
_This will be the King of all rankings. We look forward to ambitious researchers._
1. [**RBI with real motion blur:heavy_check_mark:: PSNR:disappointed:>=28.5dB**](#rbi-with-real-motion-blurheavy_check_mark-psnrdisappointed285db)
1. **RBI with real motion blur:heavy_check_mark:: SSIM:disappointed:** (to do)
1. **Adobe240 (640×352) with synthetic motion blur:bangbang:: LPIPS:heart_eyes:** (no data)  
1. [**Adobe240 (640×352) with synthetic motion blur:bangbang:: PSNR:disappointed:>=33.3dB**](#adobe240-640352-with-synthetic-motion-blurbangbang-psnrdisappointed333db)
1. **Adobe240 (640×352) with synthetic motion blur:bangbang:: SSIM:disappointed:** (to do)
1. **Adobe240 (5:8) with synthetic motion blur:bangbang:: LPIPS:heart_eyes:** (no data)
1. [**Adobe240 (5:8) with synthetic motion blur:bangbang:: PSNR:disappointed:>=25dB**](#adobe240-58-with-synthetic-motion-blurbangbang-psnrdisappointed25db)
1. **Adobe240 (5:8) with synthetic motion blur:bangbang:: SSIM:disappointed:** (to do)
### Video Deblurring Rankings
- (to do)
### Video Frame Interpolation Rankings
10. [**Vimeo-90K triplet: LPIPS:heart_eyes:(SqueezeNet)<=0.014**](#vimeo-90k-triplet-lpipsheart_eyessqueezenet0014)
10. [**Vimeo-90K triplet: LPIPS:heart_eyes:<=0.016**](#vimeo-90k-triplet-lpipsheart_eyes0016)
10. [**Vimeo-90K triplet: PSNR:disappointed:>=36dB**](#vimeo-90k-triplet-psnrdisappointed36db)
10. [**Vimeo-90K triplet: SSIM:disappointed:>=0.98**](#vimeo-90k-triplet-ssimdisappointed098)
10. [**Vimeo-90K septuplet: LPIPS:heart_eyes:<=0.032**](#vimeo-90k-septuplet-lpipsheart_eyes0032)
10. [**Vimeo-90K septuplet: PSNR:disappointed:>=36dB**](#vimeo-90k-septuplet-psnrdisappointed36db)
10. [**Vimeo-90K septuplet: SSIM:disappointed:>=0.975**](#vimeo-90k-septuplet-ssimdisappointed0975)
### Appendices
- **Rules for qualifying models for the rankings** (to do)

--------------------

## RBI with real motion blur:heavy_check_mark:: PSNR:disappointed:>=28.5dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | Pre-BiT++ |  **31.32dB** [^33] | November 2022 [^33] | [PyTorch](https://github.com/zzh-tech/BiT) ![Github stars](https://img.shields.io/github/stars/zzh-tech/BiT) | [<img alt="Request" width="40px" src="cat.png">](https://github.com/zzh-tech/BiT/issues/5) | - |
| 2 | DeMFI-Net<sub>*rb*</sub>(5,3) |  **29.03dB** [^33] | November 2021 [^34] | [PyTorch](https://github.com/JihyongOh/DeMFI) ![Github stars](https://img.shields.io/github/stars/JihyongOh/DeMFI) | - | - |
| 3 | PRF<sub>4</sub> -*Large* |  **28.55dB** [^33] | February 2020 [^35] | [PyTorch](https://github.com/laomao0/BIN) ![Github stars](https://img.shields.io/github/stars/laomao0/BIN) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Adobe240 (640×352) with synthetic motion blur:bangbang:: PSNR:disappointed:>=33.3dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | BiT++ |  **34.97dB** [^33] | November 2022 [^33] | [PyTorch](https://github.com/zzh-tech/BiT) ![Github stars](https://img.shields.io/github/stars/zzh-tech/BiT) | [<img alt="Request" width="40px" src="cat.png">](https://github.com/zzh-tech/BiT/issues/5) | - |
| 2 | DeMFI-Net<sub>*rb*</sub>(5,3) |  **34.34dB** [^34] | November 2021 [^34] | [PyTorch](https://github.com/JihyongOh/DeMFI) ![Github stars](https://img.shields.io/github/stars/JihyongOh/DeMFI) | - | - |
| 3 | ALANET |  **33.34dB** [^37] | August 2020 [^37] | [PyTorch](https://github.com/agupt013/ALANET) ![Github stars](https://img.shields.io/github/stars/agupt013/ALANET) | - | - |
| 4 | PRF<sub>4</sub> -*Large* |  **33.32dB** [^38] | February 2020 [^35] | [PyTorch](https://github.com/laomao0/BIN) ![Github stars](https://img.shields.io/github/stars/laomao0/BIN) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Adobe240 (5:8) with synthetic motion blur:bangbang:: PSNR:disappointed:>=25dB
| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | VIDUE |  **28.74dB** [^39] | March 2023 [^39] | [PyTorch](https://github.com/shangwei5/VIDUE) ![Github stars](https://img.shields.io/github/stars/shangwei5/VIDUE) | - | - |
| 2 | FLAVR |  **27.23dB** [^39] | December 2020 [^9] | [PyTorch](https://github.com/tarun005/FLAVR) ![Github stars](https://img.shields.io/github/stars/tarun005/FLAVR) | - | - |
| 3 | UTI-VFI |  **26.69dB** [^39] | December 2020 [^40] | [PyTorch](https://github.com/yjzhang96/UTI-VFI) ![Github stars](https://img.shields.io/github/stars/yjzhang96/UTI-VFI) | - | - |
| 4 | DeMFI |  **25.71dB** [^39] | November 2021 [^34] | [PyTorch](https://github.com/JihyongOh/DeMFI) ![Github stars](https://img.shields.io/github/stars/JihyongOh/DeMFI) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K triplet: LPIPS:heart_eyes:(SqueezeNet)<=0.014
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | CDFI w/ adaP/U |  **0.008** [^23] | March 2021 [^24] | [PyTorch](https://github.com/tding1/CDFI) ![Github stars](https://img.shields.io/github/stars/tding1/CDFI) | - | - |
| 2 | EDSC_s-𝓛<sub>*F*</sub> |  **0.010** [^24] | June 2020 [^25] | [PyTorch](https://github.com/Xianhang/EDSC-pytorch) ![Github stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |
| 3 | DRVI |  **0.013** [^26] | August 2021 [^26] | - | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K triplet: LPIPS:heart_eyes:<=0.016
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | EAFI-𝓛<sub>*ecp*</sub> |  **0.012** [^8] | July 2022 [^8] | - | - | - |
| 2 | SoftSplat - 𝓛<sub>*F*</sub> |  **0.013** [^15] | March 2020 [^15] | [PyTorch](https://github.com/sniklaus/softmax-splatting) ![Github stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting) | - | - |
| 3 | EDSC_s-𝓛<sub>*F*</sub> |  **0.016** [^25] | June 2020 [^25] | [PyTorch](https://github.com/Xianhang/EDSC-pytorch) ![Github stars](https://img.shields.io/github/stars/Xianhang/EDSC-pytorch) | [EDSC_s-𝓛<sub>*F*</sub>](https://github.com/Xianhang/EDSC-pytorch#pre-trained-models) | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K triplet: PSNR:disappointed:>=36dB

| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | MA-CSPA triplet-trained |  **36.76dB** [^3] | March 2022 [^3] | - | - | - |
| 2 | EMA-VFI |  **36.64dB** [^22] | March 2023 [^22] | [PyTorch](https://github.com/MCG-NJU/EMA-VFI) ![Github stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI) | - | - |
| 3 | DQBC-Aug |  **36.57dB** [^36] | April 2023 [^36] | [PyTorch](https://github.com/kinoud/DQBC) ![Github stars](https://img.shields.io/github/stars/kinoud/DQBC) | - | - |
| 4 | TTVFI |  **36.54dB** [^4] | July 2022 [^4] | - | - | - |
| 5 | AMT-G |  **36.53dB** [^31] | April 2023 [^31] | [PyTorch](https://github.com/MCG-NKU/AMT) ![Github stars](https://img.shields.io/github/stars/MCG-NKU/AMT) | - | - |
| 6-7 | AdaFNIO |  **36.50dB** [^19] | November 2022 [^19] | [PyTorch](https://github.com/HrishikeshVish/AdaFNIO) ![Github stars](https://img.shields.io/github/stars/HrishikeshVish/AdaFNIO) | - | - |
| 6-7 | VFIformer |  **36.50dB** [^6] | May 2022 [^6] | [PyTorch](https://github.com/dvlab-research/VFIformer) ![Github stars](https://img.shields.io/github/stars/dvlab-research/VFIformer) | - | - |
| 8 | FGDCN-L |  **36.46dB** [^21] | November 2022 [^21] | [TBD](https://github.com/lpcccc-cv/FGDCN) ![Github stars](https://img.shields.io/github/stars/lpcccc-cv/FGDCN) | - | - |
| 9 | UPR-Net LARGE |  **36.42dB** [^18] | November 2022 [^18] | [PyTorch](https://github.com/srcn-ivl/UPR-Net) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net) | - | - |
| 10 | EAFI-𝓛<sub>*ecc*</sub> |  **36.38dB** [^8] | July 2022 [^8] | - | - | - |
| 11 | H-VFI-Large |  **36.37dB** [^20] | November 2022 [^20] | - | - | - |
| 12 | NCM-Large |  **36.22dB** [^32] | July 2022 [^32] | - | - | - |
| 13 | IFRNet large |  **36.20dB** [^10] | May 2022 [^10] | [PyTorch](https://github.com/ltkong218/IFRNet) ![Github stars](https://img.shields.io/github/stars/ltkong218/IFRNet) | - | - |
| 14-15 | EBME-H* |  **36.19dB** [^11] | June 2022 [^11] | [PyTorch](https://github.com/srcn-ivl/EBME) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/EBME) | - | - |
| 14-15 | RIFE-Large |  **36.19dB** [^12] | November 2020 [^12] | [PyTorch](https://github.com/megvii-research/ECCV2022-RIFE) ![Github stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE) | [RIFE v4.6;<br />v4.5; v4.4;<br />v4.3; v4.2;<br />v3.8; v3.1](https://github.com/hzwer/Practical-RIFE#model-list)<br />![Github stars](https://img.shields.io/github/stars/hzwer/Practical-RIFE) | [TensorRT;<br />ONNX;<br />OpenVINO](https://github.com/AmusementClub/vs-mlrt)<br />![Github stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt)<br />[TensorRT](https://github.com/HolyWu/vs-rife)<br />![Github stars](https://img.shields.io/github/stars/HolyWu/vs-rife)<br />[ncnn](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[ncnn](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 16 | ABME |  **36.18dB** [^13] | August 2021 [^13] | [PyTorch](https://github.com/JunHeum/ABME) ![Github stars](https://img.shields.io/github/stars/JunHeum/ABME) | - | - |
| 17 | SoftSplat - 𝓛<sub>*Lap*</sub> |  **36.10dB** [^15] | March 2020 [^15] | [PyTorch](https://github.com/sniklaus/softmax-splatting) ![Github stars](https://img.shields.io/github/stars/sniklaus/softmax-splatting) | - | - |
| 18 | FILM-𝓛<sub>1</sub> |  **36.06dB** [^16] | February 2022 [^16] | [TensorFlow](https://github.com/google-research/frame-interpolation) ![Github stars](https://img.shields.io/github/stars/google-research/frame-interpolation) | [FILM-𝓛<sub>*S*</sub>;<br />FILM-𝓛<sub>VGG</sub>](https://github.com/google-research/frame-interpolation#pre-trained-models) | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K triplet: SSIM:disappointed:>=0.98

| Rank | Model | SSIM ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | AMT-G |  **0.982** [^31] | April 2023 [^31] | [PyTorch](https://github.com/MCG-NKU/AMT) ![Github stars](https://img.shields.io/github/stars/MCG-NKU/AMT) | - | - |
| 2-3 | EMA-VFI |  **0.9819** [^22] | March 2023 [^22] | [PyTorch](https://github.com/MCG-NJU/EMA-VFI) ![Github stars](https://img.shields.io/github/stars/MCG-NJU/EMA-VFI) | - | - |
| 2-3 | TTVFI |  **0.9819** [^4] | July 2022 [^4] | - | - | - |
| 4 | DQBC-Aug |  **0.9817** [^36] | April 2023 [^36] | [PyTorch](https://github.com/kinoud/DQBC) ![Github stars](https://img.shields.io/github/stars/kinoud/DQBC) | - | - |
| 5 | VFIformer |  **0.9816** [^6] | May 2022 [^6] | [PyTorch](https://github.com/dvlab-research/VFIformer) ![Github stars](https://img.shields.io/github/stars/dvlab-research/VFIformer) | - | - |
| 6 | UPR-Net LARGE |  **0.9815** [^18] | November 2022 [^18] | [PyTorch](https://github.com/srcn-ivl/UPR-Net) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/UPR-Net) | - | - |
| 7 | FGDCN-L |  **0.9814** [^21] | November 2022 [^21] | [TBD](https://github.com/lpcccc-cv/FGDCN) ![Github stars](https://img.shields.io/github/stars/lpcccc-cv/FGDCN) | - | - |
| 8-10 | EBME-H* |  **0.981** [^11] | June 2022 [^11] | [PyTorch](https://github.com/srcn-ivl/EBME) ![Github stars](https://img.shields.io/github/stars/srcn-ivl/EBME) | - | - |
| 8-10 | H-VFI-Large |  **0.981** [^20] | November 2022 [^20] | - | - | - |
| 8-10 | RIFE-Large |  **0.981** [^12] | November 2020 [^12] | [PyTorch](https://github.com/megvii-research/ECCV2022-RIFE) ![Github stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE) | [RIFE v4.6;<br />v4.5; v4.4;<br />v4.3; v4.2;<br />v3.8; v3.1](https://github.com/hzwer/Practical-RIFE#model-list)<br />![Github stars](https://img.shields.io/github/stars/hzwer/Practical-RIFE) | [TensorRT;<br />ONNX;<br />OpenVINO](https://github.com/AmusementClub/vs-mlrt)<br />![Github stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt)<br />[TensorRT](https://github.com/HolyWu/vs-rife)<br />![Github stars](https://img.shields.io/github/stars/HolyWu/vs-rife)<br />[ncnn](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[ncnn](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 11 | IFRNet large |  **0.9808** [^10] | May 2022 [^10] | [PyTorch](https://github.com/ltkong218/IFRNet) ![Github stars](https://img.shields.io/github/stars/ltkong218/IFRNet) | - | - |
| 12 | NCM-Large |  **0.9807** [^32] | July 2022 [^32] | - | - | - |
| 13 | ABME |  **0.9805** [^13] | August 2021 [^13] | [PyTorch](https://github.com/JunHeum/ABME) ![Github stars](https://img.shields.io/github/stars/JunHeum/ABME) | - | - |
| 14 | MA-CSPA triplet-trained |  **0.980** [^3] | March 2022 [^3] | - | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K septuplet: LPIPS:heart_eyes:<=0.032
| Rank | Model | LPIPS ↓ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | RIFE |  **0.0233** [^27] | November 2020 [^12] | [PyTorch](https://github.com/megvii-research/ECCV2022-RIFE) ![Github stars](https://img.shields.io/github/stars/megvii-research/ECCV2022-RIFE) | [RIFE v4.6;<br />v4.5; v4.4;<br />v4.3; v4.2;<br />v3.8; v3.1](https://github.com/hzwer/Practical-RIFE#model-list)<br />![Github stars](https://img.shields.io/github/stars/hzwer/Practical-RIFE) | [TensorRT;<br />ONNX;<br />OpenVINO](https://github.com/AmusementClub/vs-mlrt)<br />![Github stars](https://img.shields.io/github/stars/AmusementClub/vs-mlrt)<br />[TensorRT](https://github.com/HolyWu/vs-rife)<br />![Github stars](https://img.shields.io/github/stars/HolyWu/vs-rife)<br />[ncnn](https://github.com/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/HomeOfVapourSynthEvolution/VapourSynth-RIFE-ncnn-Vulkan)<br />[ncnn](https://github.com/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan)<br />![Github stars](https://img.shields.io/github/stars/styler00dollar/VapourSynth-RIFE-ncnn-Vulkan) |
| 2 | IFRNet |  **0.0274** [^27] | May 2022 [^10] | [PyTorch](https://github.com/ltkong218/IFRNet) ![Github stars](https://img.shields.io/github/stars/ltkong218/IFRNet) | - | - |
| 3 | VFIT-B | **0.0304** [^27] | November 2021 [^2] | [PyTorch](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) ![Github stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 4 | ABME |  **0.0309** [^27] | August 2021 [^13] | [PyTorch](https://github.com/JunHeum/ABME) ![Github stars](https://img.shields.io/github/stars/JunHeum/ABME) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K septuplet: PSNR:disappointed:>=36dB

| Rank | Model | PSNR ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1 | JNMR | **37.09dB** [^1] | June 2022 [^1] | [TBD](https://github.com/ruhig6/JNMR) ![Github stars](https://img.shields.io/github/stars/ruhig6/JNMR) | - | - |
| 2 | VFIT-B | **36.96dB** [^2] | November 2021 [^2] | [PyTorch](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) ![Github stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 3 | VRT |  **36.53dB** [^5] | June 2022 (VFI) [^5] | [PyTorch](https://github.com/JingyunLiang/VRT) ![Github stars](https://img.shields.io/github/stars/JingyunLiang/VRT) | - | - |
| 4 | MA-CSPA septuplet-trained |  **36.50dB** [^3] | March 2022 [^3] | - | - | - |
| 5 | ST-MFNet | **36.45dB** [^1] | November 2021 [^7] | [PyTorch](https://github.com/danielism97/ST-MFNet) ![Github stars](https://img.shields.io/github/stars/danielism97/ST-MFNet) | - | - |
| 6 | FLAVR |  **36.25dB** [^9] | December 2020 [^9] | [PyTorch](https://github.com/tarun005/FLAVR) ![Github stars](https://img.shields.io/github/stars/tarun005/FLAVR) | - | - |
| 7 | DBVI |  **36.17dB** [^17] | October 2022 [^17] | [PyTorch](https://github.com/Oceanlib/DBVI) ![Github stars](https://img.shields.io/github/stars/Oceanlib/DBVI) | - | - |
| 8 | EDC | **36.14dB** [^1] | February 2022 [^14] | [PyTorch](https://github.com/danielism97/EDC) ![Github stars](https://img.shields.io/github/stars/danielism97/EDC) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

## Vimeo-90K septuplet: SSIM:disappointed:>=0.975

| Rank | Model | SSIM ↑ | Originally<br />announced | Official<br />repository | Practical<br />models | VapourSynth |
|:----:|:----|:----:|:----:|:----:|:----:|:----:|
| 1-2 | JNMR | **0.978** [^1] | June 2022 [^1] | [TBD](https://github.com/ruhig6/JNMR) ![Github stars](https://img.shields.io/github/stars/ruhig6/JNMR) | - | - |
| 1-2 | VFIT-B | **0.978** [^2] | November 2021 [^2] | [PyTorch](https://github.com/zhshi0816/Video-Frame-Interpolation-Transformer) ![Github stars](https://img.shields.io/github/stars/zhshi0816/Video-Frame-Interpolation-Transformer) | - | - |
| 3 | VRT |  **0.977** [^5] | June 2022 (VFI) [^5] | [PyTorch](https://github.com/JingyunLiang/VRT) ![Github stars](https://img.shields.io/github/stars/JingyunLiang/VRT) | - | - |
| 4-5 | DBVI |  **0.976** [^17] | October 2022 [^17] | [PyTorch](https://github.com/Oceanlib/DBVI) ![Github stars](https://img.shields.io/github/stars/Oceanlib/DBVI) | - | - |
| 4-5 | ST-MFNet | **0.976** [^1] | November 2021 [^7] | [PyTorch](https://github.com/danielism97/ST-MFNet) ![Github stars](https://img.shields.io/github/stars/danielism97/ST-MFNet) | - | - |
| 6 | FLAVR |  **0.975** [^9] | December 2020 [^9] | [PyTorch](https://github.com/tarun005/FLAVR) ![Github stars](https://img.shields.io/github/stars/tarun005/FLAVR) | - | - |

[[Back to Top]](#video-frame-interpolation-rankingsand-video-deblurring-rankings)
[[Back to the List of Rankings]](#list-of-rankings)

[^1]: JNMR: Joint Non-linear Motion Regression for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2206.04231)
[^2]: Video Frame Interpolation Transformer [[CVPR 2022]](https://openaccess.thecvf.com/content/CVPR2022/html/Shi_Video_Frame_Interpolation_Transformer_CVPR_2022_paper.html) [[arXiv]](https://arxiv.org/abs/2111.13817)
[^3]: Exploring Motion Ambiguity and Alignment for High-Quality Video Frame Interpolation [[CVPR 2023]](https://openaccess.thecvf.com/content/CVPR2023/html/Zhou_Exploring_Motion_Ambiguity_and_Alignment_for_High-Quality_Video_Frame_Interpolation_CVPR_2023_paper.html) [[arXiv]](https://arxiv.org/abs/2203.10291)
[^4]: TTVFI: Learning Trajectory-Aware Transformer for Video Frame Interpolation [[arXiv]](https://arxiv.org/abs/2207.09048)
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
[^28]: Image Deblurring with Domain Generalizable Diffusion Models [[arXiv]](https://arxiv.org/abs/2212.01789)
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
