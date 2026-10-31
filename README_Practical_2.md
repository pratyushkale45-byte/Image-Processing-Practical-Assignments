# Digital Image Processing – Assignment 2

## Overview

This Jupyter Notebook contains six practical problems covering image analysis, edge detection, compression, JPEG-style processing, texture analysis, and image segmentation.

The notebook is titled **Assignment 2: Digital Image Processing** and is saved as `IPP assisngment 3 (1).ipynb`.

## Assignment Problems

### Problem 1: Comparative Edge Detection on Natural Images
- Load an outdoor natural image.
- Apply Sobel, Laplacian, and Canny edge detection.
- Compare the edge maps and discuss which operator captures the most meaningful edges.

### Problem 2: Noise Sensitivity Experiment
- Add Gaussian noise and salt-and-pepper noise to a clean grayscale image.
- Apply Sobel and Laplacian edge detection to clean and noisy images.
- Compare noise sensitivity and edge clarity.
- Apply Gaussian and median filtering as preprocessing and compare the results.

### Problem 3: Compression Ratio Comparison (RLE vs Huffman)
- Load a grayscale image with large smooth regions.
- Implement Run-Length Encoding (RLE) and Huffman Coding.
- Compare bit-length before and after compression and percentage reduction.
- Explain the performance of each compression method.

### Problem 4: JPEG Block Artifact Analysis
- Implement an 8 × 8 block-based JPEG-style compression pipeline using 2D DCT and quantization.
- Test low, medium, and high quantization levels.
- Examine block artifacts and texture/detail loss.
- Compare image quality using PSNR and SSIM.

### Problem 5: Texture-Based Segmentation using GLCM Features
- Extract Gray-Level Co-occurrence Matrix (GLCM) features: contrast, energy, and homogeneity.
- Apply K-Means clustering with k = 3.
- Compare feature maps and segmentation results.
- Observe how feature selection affects segmentation quality.

### Problem 6: Multi-Feature Segmentation for Disease Detection
- Load a plant or skin lesion image.
- Construct features using intensity, Sobel gradient magnitude, and local texture variance.
- Standardize the feature values and apply K-Means clustering with k = 3.
- Evaluate how the features separate diseased and healthy-looking regions and identify possible misclassifications.

## Technologies and Libraries

- **Python 3** – Programming language
- **Jupyter Notebook** – Interactive development environment
- **OpenCV (`opencv-python`)** – Image loading, filtering, edge detection, colour conversion, and DCT-related processing
- **NumPy** – Numerical and array operations
- **Matplotlib** – Image and result visualization
- **Pillow (`PIL`)** – Image handling
- **scikit-image** – GLCM features, PSNR, and SSIM metrics
- **scikit-learn** – Feature standardization and K-Means clustering

## Project Structure

```text
Digital-Image-Processing-Assignment/
│
├── IPP assisngment 3 (1).ipynb
├── natural_image.jpg
├── document_image.png
├── texture_image.png
└── plant_disease.jpg
```

Some notebook sections download sample images automatically when the corresponding file is missing. Other sections expect the required image to already be present in the notebook's working directory. Check the image-loading cells and ensure the expected files are available before running the notebook.

## Setup and Installation

1. Install Python 3.
2. Install the required packages:

```bash
pip install opencv-python numpy matplotlib pillow scikit-image scikit-learn jupyter
```

3. Open a terminal in the project folder.
4. Start Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `IPP assisngment 3 (1).ipynb`.
6. Run the notebook cells in order.

## Expected Outputs

The notebook is designed to produce:

- Original image and Sobel, Laplacian, and Canny edge maps.
- Comparisons of edge detection under Gaussian and salt-and-pepper noise, before and after filtering.
- RLE and Huffman compression measurements and comparison.
- JPEG-style compressed images at different quantization levels, with PSNR and SSIM measurements.
- GLCM feature maps and K-Means texture segmentation results.
- Multi-feature K-Means segmentation results for a plant or skin lesion image.

## Important Notes

- Run cells in order because later problems reuse images and variables created earlier in the notebook.
- Keep the input images in the notebook's working directory unless the relevant cell downloads them.
- The JPEG block-processing section uses `natural_image.jpg`, so that image must be available after Problem 1.
- The RLE/Huffman and GLCM sections use image inputs such as `document_image.png` and `texture_image.png`; verify that these files exist before running those sections.
- Internet access may be required for notebook cells that download sample images.
- The notebook describes segmentation clusters; a cluster label alone should not be treated as a medical diagnosis.

## Learning Outcomes

After completing this assignment, you should be able to:

- Compare common edge-detection operators.
- Evaluate how image noise affects edge detection.
- Apply basic lossless compression techniques and compare their compression ratios.
- Understand block-based DCT and quantization in JPEG-style compression.
- Measure image quality using PSNR and SSIM.
- Extract GLCM texture features.
- Use feature scaling and K-Means clustering for image segmentation.

---

**Assignment:** Digital Image Processing – Assignment 2  
**Notebook:** `IPP assisngment 3 (1).ipynb`
