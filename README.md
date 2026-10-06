**Overview**

This project was developed as part of my *MSc Data Science dissertation at the University of Wolverhampton*.
The project focuses on satellite-based land-cover classification using *deep learning and machine learning techniques*. A *U-Net convolutional neural network* was implemented for pixel-wise semantic segmentation of multispectral satellite imagery, with a **Random Forest** model used as a classical machine-learning baseline.
The project uses *Sentinel-2 Level-2A multispectral imagery* together with **ESA WorldCover** land-cover labels.


**Objectives**

The main objectives of this project were to:
- Develop an end-to-end satellite image classification pipeline.
- Perform land-cover classification using multispectral Sentinel-2 imagery.
- Implement a U-Net model for pixel-wise semantic segmentation.
- Develop a Random Forest baseline for comparison.
- Evaluate model performance using classification metrics and visualisation.
- Investigate the challenges associated with satellite-based land-cover classification.


**Dataset**

The project uses:

- *Sentinel-2 Level-2A* multispectral satellite imagery
- *ESA WorldCover* land-cover labels

The original datasets are **not included in this repository** because of their large file size.


**Methodology**

The overall workflow consists of:
1. Sentinel-2 band extraction
2. Spectral data preprocessing and normalisation
3. Land-cover label reprojection
4. Patch generation
5. Training dataset preparation
6. U-Net model training
7. Random Forest baseline classification
8. Full-scene inference
9. Model evaluation
10. Visualisation of classification results


**Models**

*U-Net*
A U-Net convolutional neural network was implemented for **semantic segmentation**, allowing the model to classify land-cover categories at pixel level.

*Random Forest*
A Random Forest classifier was implemented as a traditional machine-learning baseline to provide a comparison with the deep learning approach.


**Results**

The experiments demonstrated several practical challenges involved in applying machine learning and deep learning to satellite-based land-cover classification.
The final experiments produced **very low full-scene accuracy and near-zero Intersection over Union (IoU)** for the tested models. Visual results also indicated over-smoothing and class collapse.
The main factors affecting performance included:
- Limited labelled training patches
- Severe class imbalance
- Downsampling of satellite imagery due to hardware limitations
- Sparse valid labels
- Patch extraction limitations
- Class-index inconsistencies during development
- Limited computational resources

Although the final classification performance was limited, the project successfully developed an **end-to-end satellite image segmentation pipeline** and provided practical insight into the challenges of working with real-world geospatial data.


**Project Structure**

Satellite-Based-Land-Cover-Classification/
│
├── Data/
│   └── Original satellite and label data
│
├── Output/
│   └── Model outputs and results
│
├── Outputs/
│   └── Additional outputs and visualisations
│
├── Module.ipynb
│   └── Main project notebook
│
├── Visualisation.ipynb
│   └── Results visualisation and analysis
│
├── Report.pdf
│   └── MSc dissertation/project report
│
└── README.md
    └── Project documentation
