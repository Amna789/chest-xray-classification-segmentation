# Chest X-Ray Disease Classification & Lung Segmentation

A medical image analysis project focused on automated **lung segmentation** and **disease classification** from chest X-ray (CXR) images.

## Project Overview

Chest X-rays are widely used for detecting and assessing various pulmonary and cardiovascular conditions. This project explores two complementary computer vision tasks:

1. **Lung Segmentation** — identifying and extracting the left and right lung regions from chest X-ray images.
2. **Disease Classification** — classifying chest X-ray images into six predefined classes.

The project was originally developed as a Digital Image Processing project and is currently being reconstructed and extended into a reproducible Python-based implementation.

## 1. Lung Segmentation

The current segmentation pipeline uses classical image-processing techniques rather than a computationally intensive convolutional neural network.

### Pipeline

```text
Chest X-ray
    ↓
Grayscale Conversion
    ↓
CLAHE Contrast Enhancement
    ↓
Otsu Thresholding
    ↓
Morphological Erosion
    ↓
Flood-Fill Background Removal
    ↓
Morphological Closing
    ↓
Contour Detection
    ↓
Selection of Lung Contours
    ↓
Morphological Dilation
    ↓
Predicted Lung Mask
```

### Techniques Used

* OpenCV
* CLAHE (Contrast Limited Adaptive Histogram Equalization)
* Otsu thresholding
* Morphological erosion
* Morphological closing
* Morphological dilation
* Flood-fill
* Contour detection

### Evaluation

The predicted lung masks are compared with corresponding ground-truth masks.

The segmentation component uses:

* **Dice coefficient**
* **Jaccard index**

The original project achieved an average:

| Metric           |    Score |
| ---------------- | -------: |
| Dice coefficient | **0.83** |
| Jaccard index    | **0.74** |

These results will be reproduced and verified as the project is reconstructed.

---

## 2. Chest X-Ray Disease Classification

The second component focuses on classifying CXRs into six predefined classes:

1. Atelectasis
2. Cardiomegaly
3. Consolidation
4. Edema
5. No Finding
6. Pleural Effusion

The original project explored multiple deep learning architectures, including pretrained and custom CNN-based models.

The classification component is currently being reconstructed and will be added to this repository after the segmentation pipeline.

### Planned Evaluation

Classification performance will be evaluated using:

* Sensitivity
* Specificity
* Overall accuracy
* Confusion matrix

---

## Dataset

The project uses separate datasets for the segmentation and classification tasks.

### Segmentation Dataset

The segmentation dataset contains chest X-ray images and corresponding lung masks. The image and mask files share corresponding filenames.

The data is divided into:

* Training set
* Validation set

### Classification Dataset

The classification dataset contains chest X-ray images organized into six disease/class categories and is divided into training and validation subsets.

> **Note:** The datasets are not included in this repository because of their size and dataset licensing/distribution considerations.

---

## Project Structure

The repository is currently under development. The structure will be expanded as the implementation is reconstructed.

```text
chest-xray-classification-segmentation/
│
├── segmentation/
│   ├── src/
│   ├── notebooks/
│   └── results/
│
├── classification/
│   ├── src/
│   ├── notebooks/
│   └── results/
│
├── README.md
└── .gitignore
```

---

## Current Status

### Lung Segmentation

* [x] Original segmentation methodology identified
* [x] Classical image-processing pipeline documented
* [x] Original Dice and Jaccard results identified
* [ ] Clean Python implementation
* [ ] Reproduce validation results
* [ ] Add sample predictions and visualizations

### Disease Classification

* [x] Six classification classes identified
* [x] Original model architectures identified
* [ ] Reconstruct classification implementation
* [ ] Reproduce validation results
* [ ] Add confusion matrices and performance metrics

---

## Technologies

* Python
* OpenCV
* NumPy
* Matplotlib
* TensorFlow
* PyTorch

---

## Project Status

**In Progress**

The lung segmentation component is being reconstructed first, followed by the disease classification component. The goal is to create a reproducible and well-documented medical image analysis pipeline from the original project.

---

## Author

**Amna Arif**

Computer & Software Engineering

GitHub: [Amna789](https://github.com/Amna789)
