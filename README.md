# CRF-Net

Cloud-Resilient Fusion Network (CRF-Net)
High-Resolution NDVI Reconstruction for Carbon Flux Assessment in Tropical Cloudy Regions

This repository provides the implementation of CRF-Net, a deep learning framework specifically designed to reconstruct high-resolution NDVI time series in tropical regions with persistent cloud cover. The approach integrates SAR backscatter features from Sentinel-1 and optical NDVI data from Sentinel-2 in a unified end-to-end architecture, enabling accurate gap-filling during extended cloudy periods and facilitating downstream ecological applications such as carbon flux estimation (NPP, Rh, NEP) and landscape pattern analysis.

Key Contributions
SAR Feature Encoder — Extracts spatial–temporal backscatter features (VV, VH) from Sentinel-1 imagery.

BiLSTM with Attention — Models long-term temporal dependencies while adaptively weighting relevant observations.

NDVI Regression Module — Generates reconstructed NDVI at 10-m spatial resolution.

Cloud-Resilient Performance — Maintains R² > 0.82 and RMSE ≈ 0.11 in tropical monsoon regions with >80% cloud cover.

Open Workflow — Fully compatible with Google Earth Engine preprocessing and standard geospatial libraries.

Model Architecture
<p align="center"> <img src="model_architecture.png" alt="CRF-Net Architecture" width="85%"> </p>
The architecture consists of a dual-branch encoder (SAR branch + temporal modeling branch) and an attention-enhanced fusion module. The SAR branch captures spatial and backscatter dynamics, while the BiLSTM-Attention branch extracts sequential patterns from multi-temporal data. The fused representation is passed to a regression layer to produce the final NDVI reconstruction.

Applications
CRF-Net supports a range of environmental monitoring and ecological modeling tasks, including:

NDVI time series reconstruction in cloudy regions.

Pixel-level carbon flux estimation (NPP, Rh, NEP) at 10-m resolution.

Landscape ecology analysis using reconstructed vegetation indices.
