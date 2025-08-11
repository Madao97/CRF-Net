<img width="3321" height="726" alt="1" src="https://github.com/user-attachments/assets/8e24a246-bc79-485f-b035-30e1c9b46037" /># CRF-Net
<img width="2029" height="2886" alt="CNN-RNN散点对比" src="https://github.com/user-attachments/assets/25e528aa-212e-4b1e-8910-d0d3b33c250a" />

**Cloud-Resilient Fusion Network (CRF-Net)**
High-Resolution NDVI Reconstruction for Carbon Flux Assessment in Tropical Cloudy Regions

This repository provides the implementation of CRF-Net, a deep learning framework specifically designed to reconstruct high-resolution NDVI time series in tropical regions with persistent cloud cover. The approach integrates SAR backscatter features from Sentinel-1 and optical NDVI data from Sentinel-2 in a unified end-to-end architecture, enabling accurate gap-filling during extended cloudy periods and facilitating downstream ecological applications such as carbon flux estimation (NPP, Rh, NEP) and landscape pattern analysis.

Key Contributions
SAR Feature Encoder — Extracts spatial–temporal backscatter features (VV, VH) from Sentinel-1 imagery.

BiLSTM with Attention — Models long-term temporal dependencies while adaptively weighting relevant observations.

NDVI Regression Module — Generates reconstructed NDVI at 10-m spatial resolution.

Cloud-Resilient Performance — Maintains R² > 0.82 and RMSE ≈ 0.11 in tropical monsoon regions with >80% cloud cover.

Open Workflow — Fully compatible with Google Earth Engine preprocessing and standard geospatial libraries.

Model Architecture
The architecture consists of a dual-branch encoder (SAR branch + temporal modeling branch) and an attention-enhanced fusion module. The SAR branch captures spatial and backscatter dynamics, while the BiLSTM-Attention branch extracts sequential patterns from multi-temporal data. The fused representation is passed to a regression layer to produce the final NDVI reconstruction.

Applications
CRF-Net supports a range of environmental monitoring and ecological modeling tasks, including:

NDVI time series reconstruction in cloudy regions.

Pixel-level carbon flux estimation (NPP, Rh, NEP) at 10-m resolution.

Landscape ecology analysis using reconstructed vegetation indices.

Data
Sentinel-1: VV & VH backscatter time series.

Sentinel-2: Cloud-masked NDVI (Level-2A, 10 m).

Temporal Coverage: 2020–2024 (example).

Spatial Resolution: 10 m, study region Kuala Selangor, Malaysia.

⚠ Due to the large size of the dataset, experimental data can be obtained upon request via email:
jiapengfei97@gmail.com
