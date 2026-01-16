# CSF Leak Total Spine MRI Protocol

This repository provides a standardized sequence details for spinal CSF leak MRI protocol designed for high-resolution evaluation of extradural CSF collections (SLEC), dural defects, and other associated spinal pathology. It is intended for radiologists, technologists, and researchers implementing or adapting advanced CSF leak imaging on clinical MRI systems.

The included protocol sheets are direct printouts from Siemens scanners, but the sequence parameters can be adapted for use on other vendors (GE, Philips) with equivalent 3D T2-weighted and bSSFP sequences.

### Sequences Included


- **3D MR Myelography**
  - *Sagittal fat-saturated 3D T2-SPACE*
  - *Compressed-sensing acceleration*
  - *0.7 mm3 isotropic resolution*
  - *For detecting SLECs*

- **Sagittal meso-scale 3D CISS**
  - *0.5 mm3 isotropic resolution*
  - *For dural defect detection*

### Potential Caveats and Workarounds

| Caveats                         | Background and Recommendations                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| High SAR warning                | Switching to low-SAR RF mode will increase TR*. While lowering the flip angle (recommended) may modestly reduce SNR, contrast remains essentially unchanged.                                                                                                                                                                                                    |
| Peripheral nerve stimulation warning | Increasing the gradient rise time is recommended to reduce peripheral nerve stimulation.                                                                                                                                                                                                                                                                     |
| Long imaging time               | Image blurring from partial Fourier imaging may obscure small dural defects and other subtle findings. Availability of parallel imaging for 3D CISS is vendor specific**. MRI scanners with high performance gradients are preferred. Sagittal (or coronal) acquisitions with a head-to-foot readout can expand coverage without increasing scan time.                     |
| Motion artifact                 | For 3D CISS, two b-SSFP datasets with opposite phase cycling are acquired and combined to suppress banding, but motion between them may introduce significant image degradation. Recommend quality control in real time of meso-CISS images and re-imaging if possible.                                                                        |
| Banding artifact                | Banding artifact worsens with B0 inhomogeneity and long TR. Use advanced shimming (e.g., absolute shim) and minimize TR to reduce banding.                                                                                                                                                                                                                      |
| Metal artifact                  | Spinal hardware may cause extensive banding artifact markedly reducing meso-CISS sensitivity for detecting dural defects. Consider alternative sequences (e.g., high-resolution T2-SPACE) or imaging at 1.5 T.                                                                                                                             |

Common technical challenges in meso-CISS imaging and recommended approaches. For additional technical details on b-SSFP, we refer readers to Bieri and Scheffler.

*Increasing TR will prolong scan time and worsen banding artifacts.

**CISS is the Siemens implementation of a balanced steady-state free-precession sequence that combines two phase-cycled acquisitions to suppress banding; vendor-specific equivalents include FIESTA-C (GE) and Phase-Balanced SARGE (Hitachi).

**Abbreviations:** b-SSFP: balanced steady-state free precession; CISS: constructive interference in steady state; RF: radiofrequency; SAR: specific absorption rate; SNR: signal-to-noise ratio; TR: repetition time.

### References:

If you use or adapt this protocol, please cite :

[Preprint] Wegscheid ML, Chatterjee AR, Raji CA, Reis MN, Fleege NP, Azad SN, Ogunlade J, Vellimana AK, Goyal MS, Nazeri A.
*Mesoscale CISS Imaging for the Detection of Dural Defects in Spinal CSF Leaks.*
medRxiv. 2025 Jul 16:2025-07. https://doi.org/10.1101/2025.07.14.25331467


