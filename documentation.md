# Documentation - Challenge Technion

## Introduction
This document describes the dataset selection process, the reasons for choosing the **Kaggle** platform, and the criteria used to determine which dataset to use in the challenge assigned by Dr. Moti Freiman for the **Technion Summer Research Program 2025**.

---

## Why Use Kaggle for Datasets?
Kaggle was chosen as the primary platform for obtaining datasets due to several technical and practical reasons:

- **Access to High-Quality Datasets:** Kaggle hosts a vast repository of high-quality public datasets frequently used for academic research and machine learning challenges.
- **Ease of Importing Data:** Kaggle provides direct API access, simplifying dataset imports into Google Colab and local development environments.
- **Scalability and Performance:** Since my local machine has limited computational power, **Kaggle-hosted datasets** allow for better performance when processed in cloud-based or optimized environments.
- **Community and Documentation:** Kaggle datasets are well-documented, often including community discussions and notebooks that aid in understanding the data structure.

---

## Dataset Selection Process
Two datasets were initially considered for this challenge, both containing MRI scans for **brain tumor detection**. After conducting an exploratory analysis, Dataset 1 was selected for further processing.

### **Dataset 1 - Selected for the Challenge**
- **Dataset Name:** Brain MRI Images for Brain Tumor Detection
- **Kaggle URL:** [Brain MRI Dataset](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection/data)
- **Reason for Selection:**
  - Clearly labeled images with **tumor** (`yes`) and **no tumor** (`no`) categories.
  - Well-structured folder hierarchy (`Training` and `Testing`), making it easier to build supervised models.
  - Suitable for classification tasks, aligning with the challenge requirements.
  - Balanced number of images between tumor and non-tumor classes.
  - Supported by existing research and community discussions.

### **Dataset 2 - Considered but Not Used**
- **Dataset Name:** Brain Tumor MRI Dataset
- **Kaggle URL:** [Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset?resource=download)
- **Reason for Discarding:**
  - Lack of clear distinction between tumor types, making interpretation difficult without a medical background.
  - Unstructured labeling, which increases preprocessing complexity.
  - No predefined `Training` and `Testing` folders, requiring additional work for dataset splitting.
  - More challenging to use in a **supervised learning** setting.

---

## Exploratory Data Analysis (EDA)
To validate the dataset selection, an **exploratory data analysis (EDA)** was conducted on Dataset 1. The following key steps were performed:

1. **Counting the Number of Images per Class:** Ensuring a balanced dataset.
2. **Visualizing Random Images:** Reviewing MRI scans for pattern consistency.
3. **Checking Image Dimensions:** Ensuring standardization of input sizes.
4. **Class Distribution Analysis:** Understanding the dataset's balance.
5. **Detecting Corrupted Images:** Verifying data integrity.
6. **Analyzing Pixel Value Distribution:** Understanding grayscale intensity variations.
7. **Comparing Patterns Between Classes:** Identifying potential differences in tumor and non-tumor images.

The full EDA code and visualizations are available in the project repository.

---

## Tools and Frameworks
This project utilizes the following tools and frameworks:

- **Google Colab & Jupyter Notebook:** Primary environments for code execution and EDA.
- **Python 3.x:** Programming language for all data processing and model training tasks.
- **Kaggle API:** Used to download datasets directly into the workspace.
- **OpenCV & Matplotlib:** Image processing and visualization.
- **Hugging Face & Ollama:** For LLM-based approaches.
- **PyTorch/TensorFlow:** Frameworks considered for future fine-tuning tasks.

---

## Dataset Access and Authentication
Since the dataset is hosted on Kaggle, an **API authentication key (kaggle.json)** is required to download it. The key is generated in your Kaggle account settings and must be placed in the correct directory:

```bash
mkdir -p ~/.kaggle
mv kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
