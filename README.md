# Hyperspectral Image Processing (Implementation from Scratch)

## View in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AshleshaShelke2004/Indian-Pines-Image-Processing/blob/main/HSI_Processing.ipynb)

## Assignment Overview
This project implements fundamental image processing and enhancement algorithms on the **Indian Pines Hyperspectral Dataset**. 

**Key Constraint:** All algorithms are implemented **from scratch** using Python and raw matrix mathematics. No high-level image processing libraries (like OpenCV, PIL, or scikit-image) were used for the core algorithms.

## Dataset
* **Target:** Indian Pines Hyperspectral Remote Sensing Scene.
* **Format:** `.mat` (Matlab data format).
* **Processing:** The code extracts a specific spectral band (Slice 100) from the 3D hyperspectral cube to apply 2D image processing techniques.

## Algorithms Implemented

### 1. Point Processing
* **Log Transform:** Dynamic range compression using the formula $s = c \cdot \log(1 + r)$.
* **Gamma Correction:** Non-linear brightness adjustment using $s = c \cdot r^\gamma$.
* **Contrast Stretching:** Linear normalization to stretch pixel intensity to the full 0-255 range.

### 2. Histogram Processing
* **Histogram Equalization:** Enhances contrast by flattening the image histogram. 
    * *Implementation:* Manually calculates the Cumulative Distribution Function (CDF) to map pixel values.

### 3. Spatial Filtering (Convolution)
* **Convolution Engine:** A manual sliding-window implementation with zero-padding to handle border pixels.
* **Mean Filter (Blur):** A 5x5 averaging kernel to reduce noise.
* **Sobel Edge Detection:** Implementation of Gradient-X and Gradient-Y kernels to calculate edge magnitude without using `cv2.Sobel`.

## Usage

1. **Environment:**
   * This code is designed to run in **Google Colab** or a standard Jupyter Notebook.

2. **Dependencies:**
   ```bash

   pip install -r requirements.txt

