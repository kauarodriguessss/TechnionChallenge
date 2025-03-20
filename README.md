# 🧠 Summer Research Application for Technion  

## 📌 Challenge Dr. Moti Freiman - Technion  

### Description  
&nbsp;&nbsp;&nbsp;&nbsp; This repository contains the challenge assigned by Dr. Moti Freiman as part of the selection process for the **Technion Summer Research Program (July 2025)**. The challenge involves working with **Large Language Models (LLMs)**, **fine-tuning** them, and performing **Exploratory Data Analysis (EDA)** on medical images.

---

## 👤 **Researcher**  
- **[Kauã Rodrigues](https://www.linkedin.com/in/kauarodrigues/)**  

---

## 🎯 **Objective of the Challenge**  
&nbsp;&nbsp;&nbsp;&nbsp; The goal of this challenge is to demonstrate my ability to handle **large language models (LLMs)**, particularly **fine-tuning** a model such as **LLaMA** to process medical image-related data.  

Key objectives include:  
- **Understanding** and processing **MRI images** of brain tumors.  
- Performing **Exploratory Data Analysis (EDA)** to extract meaningful insights.  
- **Utilizing LLMs (local execution via Ollama)** to analyze and enhance results.  
- Implementing **fine-tuning techniques** to improve model performance.  
- Structuring and documenting the entire process using **CRISP-DM methodology**.  

---

## **Project Structure**  

### **📂 1. Dataset Selection & Justification**  
- **Dataset Source**: [Brain MRI Images for Brain Tumor Detection (Kaggle)](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)  
- **Selection Justification**:  
  - The dataset contains MRI brain scans categorized into **tumor** and **non-tumor** classes.
  - It is well-structured, labeled, and supports **supervised learning**.
  - Facilitates **binary classification** and enables further enhancements through fine-tuning.

---

### **2. Exploratory Data Analysis (EDA)**  
&nbsp;&nbsp;&nbsp;&nbsp; EDA helps in understanding the dataset's structure and ensuring its suitability for model training. The analysis includes:  
- **Class Distribution**: Checking for dataset balance (tumor vs. non-tumor).  
- **Visualizing Images**: Random samples from each class.  
- **Checking Image Dimensions**: Ensuring consistency in data preprocessing.  
- **Detecting Corrupt Images**: Identifying and removing problematic samples.  
- **Pixel Distribution Analysis**: Understanding intensity variations.  
- **Comparing Patterns Between Classes**: Detecting visual differences between tumor and non-tumor images.  

---

### **3. LLM Model Usage**  
&nbsp;&nbsp;&nbsp;&nbsp; To enhance the analysis, I will leverage **local execution of LLMs**, including:  

#### **📌 Using Ollama (Local LLM Execution)**  
- Running **lightweight LLM models** locally to process text-related metadata.  
- Testing **LLM integration** with MRI dataset analysis.  

#### **📌 Alternative Approach: Hugging Face**  
- Exploring **pre-trained LLaMA models** on **Hugging Face**.  
- Comparing **fine-tuned vs. non-fine-tuned models**.  

---

### **4. Fine-Tuning Process**  
&nbsp;&nbsp;&nbsp;&nbsp; Fine-tuning aims to **adapt LLaMA models** to better handle medical imaging datasets.

- **Dataset Preparation for Fine-Tuning**  
  - Structuring MRI images in a format suitable for model training.  
  - Exploring **text-to-image** interactions to enhance model learning.  

- **Fine-Tuning Steps**  
  - Selecting the **pre-trained LLaMA version**.  
  - Training on **medical imaging-related textual data**.  
  - Evaluating results **before and after fine-tuning**.  

---

## 📌 **Methodology: CRISP-DM**  
&nbsp;&nbsp;&nbsp;&nbsp; For structuring the research, I will use the CRISP-DM (Cross Industry Standard Process for Data Mining) methodology, is widely recognized in data science projects and provides a flexible and iterative framework that allows project members to have a clear and organized view of the predictive model development process—from the initial phase of business understanding to the final deployment phase.
&nbsp;&nbsp;&nbsp;&nbsp; CRISP-DM was chosen for its ability to adapt to the needs of each project, offering a process-oriented approach divided into six key stages. Each of these stages is critical to the success of the predictive model, enabling the cycle to be revisited whenever necessary to ensure the quality and accuracy of the results.

Which consists of:  
1️⃣ **Business Understanding**: Define research goals.  
2️⃣ **Data Understanding**: Conduct EDA on the MRI dataset.  
3️⃣ **Data Preparation**: Preprocess and clean the data.  
4️⃣ **Modeling**: Train an LLM model (Ollama / Hugging Face).  
5️⃣ **Evaluation**: Analyze model performance.  
6️⃣ **Deployment**: Document and report findings.  

---

## 📂 **Dataset & Kaggle API**  
&nbsp;&nbsp;&nbsp;&nbsp; To access the dataset, I used the **Kaggle API**, which requires authentication via `kaggle.json`.  

**Why this approach?**  
- Ensures **direct access to the latest dataset version**.  
- Enables **automated downloading and version control**.  

**⚠️ Important:** The `kaggle.json` file is **not included in this repository** for security reasons. If you want to run the code, follow these steps:  
1. Create an account on [Kaggle](https://www.kaggle.com/).  
2. Go to your profile settings → Create API token.  
3. Download `kaggle.json` and place it in your working directory.  
4. Run the following command in Google Colab:  

```python
from google.colab import files
files.upload()
