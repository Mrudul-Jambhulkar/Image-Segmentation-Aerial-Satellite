# Dual Degree Project 
## Image Segmentation in Aerial and Satellite Imagery

This repository contains the work carried out as part of my **Dual Degree Project (DDP) **, focused on **image segmentation in aerial and satellite images**.  
The project explores and compares **multiple deep learning models** across **different image modalities**, including:

- **RGB**
- **Multispectral**
- **Hyperspectral**

The objective is to study how segmentation performance varies with modality, model architecture, and learning strategy, especially in **agricultural and remote sensing scenarios**.

---

## Repository Structure


---

## Folder Descriptions

### 1. `SAM-DBSCAN/`

This folder contains experiments combining **Segment Anything Model (SAM)** with **unsupervised clustering** for semantic segmentation.

**Key details:**
- SAM is used to generate object-level masks.
- **Semantic segmentation** is performed using **DBSCAN clustering**.
- **NDVI (Normalized Difference Vegetation Index)** is used as the clustering feature.
- Works on **unlabelled multispectral data**.

**Dataset:**
- Field images from **Malegaon region**
- Image size: `512 × 512`
- **4-band multispectral images**
- No ground-truth annotations

**Contents:**
- Python script implementing the SAM + DBSCAN pipeline
- Sample result images

---

### 2. `agrivision/`

This folder focuses on **supervised semantic segmentation** using the **AgriVision dataset**.

**Approach:**
- Model : **DeepLabV3+**
- Integration of an **Adaptive Class Weighting Loss Function** to address **severe class imbalance** in agricultural segmentation tasks

**Contents:**
- Python training and evaluation scripts for DeepLabV3+
- Loss function implementation and training pipeline

---

### 3. `hyperspectral3Dunet/`

This folder contains work on **hyperspectral image segmentation** using a **3D U-Net architecture**.

**Approach:**
- Hyperspectral bands are stacked to form a **volumetric (3D) image**
- **3D U-Net** integrated with a **Spectral Attention Module** (squeeze-and-excitation block)
- Dimensionality reduction using **PCA**

**Dataset:**
- Location: Field area in Shenzhou City, China
- Image size: `96 × 96`
- Original bands: `200`
- Reduced bands: `30` (using PCA)
- Number of classes: `30 crop classes`

**Contents:**
- Python scripts for preprocessing, PCA, training, and evaluation

---

### 4. `phenobench/`

This folder contains experiments on the **PhenoBench dataset** for crop field segmentation.

**Dataset:**
- Image size: `1024 × 1024`
- Modality: **RGB**
- Classes: `Crop`, `Weed`, `Soil`

**Models used:**
- **MSCG-Net**  
  *(Multi-view Self-Constructing Graph Convolutional Neural Network)*
- **DeepLabV3**

**Contents:**
- Python scripts for training and evaluation on PhenoBench
- Model-specific training pipelines

---

## Reports

- `DDP_report_stage1.pdf`  
  → Detailed documentation of **Stage 1 methodology, datasets, experiments, and results**

- `RGSTC_Report_ddp.pdf`  
  → Additional project report (RGSTC)

---



