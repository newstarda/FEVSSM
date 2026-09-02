# FEVSSM

Official project page for **Frequency-Domain Enhanced Visual State Space Model with Selective Channel Refining for Image Deblurring**.

## Current availability

The pretrained weights listed below are publicly available through file-specific Google Drive links. The weight files are not duplicated in this GitHub repository. The complete training and inference source code, together with auxiliary reproducibility materials, will be released in this repository immediately after the paper is formally accepted.

## Pre-trained Models

| Task | Evaluation / training setting | Checkpoint | Size | Download |
| :-- | :-- | :-- | --: | :-- |
| Image deblurring | GoPro | `net_g_GoPro.pth` | 149.81 MB | [Google Drive](https://drive.google.com/file/d/1uvzqm8Wd4SVvZPAV4W6OwYWlMmDB3jb_/view?usp=sharing) |
| Image deblurring | DPDD (dual-pixel) | `net_g_DPDD_D.pth` | 149.81 MB | [Google Drive](https://drive.google.com/file/d/1uhMtiblq3UYQckNkgfY6agDYnejS-wx5/view?usp=sharing) |
| Image deblurring | DPDD (single-pixel) | `net_g_DPDD_S.pth` | 149.81 MB | [Google Drive](https://drive.google.com/file/d/1nvFWhsvJ3nLLF8jj5LBZJCaPFQgU6wr9/view?usp=sharing) |
| Image deblurring | RealBlur-J | `net_g_RealBlur_J.pth` | 149.81 MB | [Google Drive](https://drive.google.com/file/d/1ophUE7mthfxL378pVmeC0FTiRzCwWMtk/view?usp=sharing) |
| Image deblurring | RealBlur-R | `net_g_RealBlur_R.pth` | 149.81 MB | [Google Drive](https://drive.google.com/file/d/1-06oTk3VFzrNKYFvJ7eN_115CbF47lhI/view?usp=sharing) |
| Image denoising (supplementary) | Denoising checkpoint supplied with the revision materials | `net_g_Denoising.pth` | 130.58 MB | [Google Drive](https://drive.google.com/file/d/1ZJTy5vBNfQSw587dfEUBQloLp1-oWXKh/view?usp=sharing) |
| Image deraining (supplementary) | Deraining checkpoint supplied with the revision materials | `net_g_Deraining.pth` | 176.44 MB | [Google Drive](https://drive.google.com/file/d/19ahofTuG13YUz3J3G-Hc7akyL3r4aL18/view?usp=sharing) |

### Checkpoint scope and verification

The five deblurring checkpoints use the FEVSSM-style checkpoint layout (`params` state dictionary, including the frequency-enhanced visual state-space blocks). `net_g_Denoising.pth` and `net_g_Deraining.pth` have different internal checkpoint layouts from the five deblurring files. They are retained here because they were supplied as supplementary-task weights, but they must **not** be described as FEVSSM checkpoints until their training code, architecture definition, and experimental provenance have been independently confirmed. The file sizes and SHA-256 digests are recorded in [models/MODEL_MANIFEST.md](models/MODEL_MANIFEST.md).

## Download and integrity check

After downloading, verify the file against the SHA-256 value in the manifest. For example:

```powershell
Get-FileHash .\models\net_g_GoPro.pth -Algorithm SHA256
```

## Google Drive publication record

The table above provides seven file-specific Google Drive links. Each checkpoint can be downloaded independently and verified against the corresponding SHA-256 digest in the model manifest.

## Code availability plan

To improve transparency and help readers inspect the reported experimental artifacts, the pretrained model weights are currently available through the file-specific Google Drive links above. This GitHub repository provides the download index and integrity information, but does not store copies of the weight files. The complete algorithm source code will be fully pushed to this repository immediately after formal acceptance of the paper, for the journal, readers, and the research community to consult and exchange. This staged release is intended to support both long-term code availability and an accurate statement of the materials currently public.

## License

This repository retains the accompanying [GNU General Public License v3.0](LICENSE). Before redistributing any supplementary checkpoint, verify that its original license permits redistribution.
