# Image Segmentation using K-Means Clustering

This repository contains a project that applies **K-Means Clustering** for unsupervised image segmentation. The goal is to identify the dominant colors in an image and use them to segment the image into regions based on these colors.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [K-Means Clustering](#k-means-clustering)
- [Results](#results)
- [License](#license)

## Overview

This project demonstrates the use of unsupervised learning (K-Means Clustering) to perform image segmentation. By clustering image pixels based on color values, the algorithm groups pixels into segments representing dominant colors. The **Elbow Method** is used to determine the optimal number of clusters.

## Dataset

- **Image for Segmentation**: The example image (elephant.jpg) used for segmentation can be downloaded from [this Google Drive link](https://drive.google.com/file/d/16iMaYEGH-GgmqZfrCTw2vjYayllcgFcb/view?usp=sharing). You can replace it with any other image as well.

## Technologies Used
- Python 3.8+
- Libraries:
  - `OpenCV` (for image processing)
  - `scikit-learn`
  - `numpy`
  - `matplotlib`

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/image-segmentation-kmeans.git
    cd image-segmentation-kmeans
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the example image from [Google Drive](https://drive.google.com/file/d/16iMaYEGH-GgmqZfrCTw2vjYayllcgFcb/view?usp=sharing) and place it in the project directory.

## Usage

1. **Run the Jupyter notebook**:
    ```bash
    jupyter notebook image-segmentation-kmeans.ipynb
    ```

2. The notebook will:
    - Load and display the input image.
    - Apply the **Elbow Method** to find the optimal number of clusters (K).
    - Perform **K-Means Clustering** on the image pixels to segment the image based on dominant colors.
    - Display the segmented image with the clustered regions.

## K-Means Clustering

- The image is first converted to RGB format and flattened into a 2D array where each row represents a pixel with 3 color channels.
- The **Elbow Method** is used to find the optimal number of clusters by plotting the Within-Cluster Sum of Squares (WCSS).
- **K-Means Clustering** is applied to segment the image into `K` regions based on color values.
- The final segmented image is displayed, where each pixel is replaced by the closest dominant color identified by the clustering algorithm.

## Results

- **Elbow Method** helps in determining the optimal number of clusters for segmentation.
- The image is segmented into regions, each corresponding to one of the dominant colors.
- The segmented image is reconstructed and displayed as a new image with simplified color regions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
