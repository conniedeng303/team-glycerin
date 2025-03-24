# Kaggle Competition - Equitable AI for Dermatology Team Glycerin 💻

## Team Members  👥
- Veronica Aragon - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/veronicaragon)  
- Connie Deng - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/conniedeng303)  
- [Teghpreet Singh Mago] - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/Teghpreet3001)  
- [Team Member 4] - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](INSERT_YOUR_LINK_HERE)  
- [Team Member 5] - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](INSERT_YOUR_LINK_HERE)  
- [Team Member 6] - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](INSERT_YOUR_LINK_HERE)  
  
---

## Project Highlights  💫
- Key takeaways from the project  
- Interesting findings or breakthroughs  
- Unique approaches or innovations implemented  

---

## Setup & Execution  📋
### **Setup**  
- Install dependencies  
- Configure Kaggle API  
- Set up Jupyter notebooks or development environment  

### **Execution**  
- How to run scripts and train models  
- Steps to evaluate model results  
- Troubleshooting common setup issues  

---

## Project Overview 👀
This Kaggle competition, part of the **Break Through Tech AI Program**, challenges teams to develop an inclusive **machine learning model** for dermatology. The competition is hosted by the **Algorithmic Justice League (AJL)** and brings together AI Fellows from the Virtual, Boston (MIT), and Los Angeles (UCLA) programs.  

### 🎯 **Objective**  
Our goal is to **train an AI model that accurately classifies 16 skin conditions across diverse skin tones** using the provided dataset. By leveraging machine learning techniques, we aim to improve dermatology AI tools that historically struggle with underrepresented skin types.  

### 🌍 **Real-World Impact**  
Dermatology AI models often **underperform for people with darker skin tones** due to **biased training data**, leading to **misdiagnosis and health disparities**. By addressing these biases, our work can:  
✅ **Improve diagnostic accuracy** for diverse populations  
✅ **Reduce healthcare inequities** caused by AI bias  
✅ **Advance fairness and transparency in AI systems**  

This project contributes to ongoing research in **ethical AI** and supports efforts to build more **inclusive, trustworthy AI models** in healthcare.  

---

## Data Exploration 🗺️
- Overview of the dataset(s) used (Kaggle-provided + any additional sources)  
- Data exploration and preprocessing methods  
- **Visualizations:**  
  - Chart 1: [Description]  
  - Chart 2: [Description]  
  - Chart 3: [Description]  

---

## Model Development  🔧
We initially experimented with various pre-trained models, including Inception, MobileNetV1 and V3, ResNet, and EfficientNet. Among them, Inception demonstrated the best out-of-the-box performance. Following this, our focus shifted primarily to testing different data augmentations (rotations, hues, brightness, etc.) with varying probabilities of application. Data augmentation provided to be the most useful at getting our score, for example, we created functions that created cutouts and noise injections within the images, which prevents the model from overfitting and helped us reach our final score

We also explored modifications at the architectural level, such as incorporating dropout to help regularize the model by preventing neurons from co-adapting too strongly. As we encountered increasing issues with overfitting, we expanded our model selection and experimented with different activation functions. Additionally, we reviewed recent machine learning research in dermatology to replicate useful methodologies—though not exactly, as many papers are tailored to specific skin conditions and do not always address our particular challenges.

One of the significant challenges we faced was the limited computational resources available on Colab. For instance, we attempted to generate synthetic images using SMOTE and GANs, but Colab's constraints prevented us from executing these techniques effectively.


---

## Results & Key Findings 🔑
![image](https://github.com/user-attachments/assets/ca078973-f30f-4dd3-a6a2-f7c83b493137)

---

## Impact Narrative 🌍
- How project findings contribute to solving the real-world problem  
- Potential applications beyond the competition  
- Ethical considerations and broader implications  

---

## Next Steps & Future Improvements 🚀
- Possible improvements for better model performance  
- Additional data sources or techniques to explore  
- Steps for future project development  

---
