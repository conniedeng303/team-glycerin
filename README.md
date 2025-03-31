# Kaggle Competition - Equitable AI for Dermatology Team Glycerin 💻

## Team Members  👥
- Veronica Aragon - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/veronicaragon)
  
- Connie Deng - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/conniedeng303)

- Samhita Reddivalam - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/samhitavt) 
  
- Teghpreet Singh Mago - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/Teghpreet3001)  

- Angela Sidhu - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/angelasidhu)  

- Kamillah Ismail - [![GitHub Profile](https://img.shields.io/badge/GitHub-Profile-000?style=flat&logo=github)](https://github.com/Kismail3)
  
---

## Project Highlights  💫

### 🔑 Key Takeaways
Throughout our project, we explored multiple pre-trained models, to develop a robust dermatology classification model. These included:
- DenseNet201
- MobileNetV3
- ResNet
- Xception
- InceptionV3

After extensive experimentation, InceptionV3 emerged as the most effective model, achieving the highest accuracy score. Our approach emphasized iterative improvements through hyperparameter tuning, data augmentation, and model ensembling. Despite computational constraints on platforms like Kaggle and Google Colab, we optimized our workflow to refine our model’s predictive performance while maintaining efficiency.

### 🔍 Interesting Findings
One of the most notable discoveries was the significant impact of data augmentation on model accuracy. Techniques such as downsizing, rotation, zoom, color enhancement, brightness adjustment, and noise injection played a crucial role in improving generalization. Our team found that even slight modifications in augmentation probabilities and combinations led to noticeable performance variations. Additionally, issues such as dataset bias and overfitting posed challenges, emphasizing the need for dermatology AI models to be trained on more diverse datasets to ensure fairness across all skin tones.

### 🚀 Innovations
To push our model’s accuracy further, we explored unique enhancements, including fine-tuning pre-trained layers, implementing dropout to prevent overfitting, and optimizing learning rates. We also attempted synthetic data generation methods like SMOTE to address class imbalances, though computational limitations prevented full implementation. Our model development process combined insights from recent AI research in dermatology with practical experimentation, ensuring that our final InceptionV3 model was both performant and adaptable.



---

## Setup & Execution  📋
### **Setup**  
- The datasets need to be downloaded following: https://www.kaggle.com/competitions/bttai-ajl-2025/data

### **Execution**  
- The code for this project lies in the model_training.ipynb notebook under the notebooks folder.

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
**Dataset Description**

The dataset used in this project is a subset of the FitzPatrick17k dataset, which contains around 17,000 dermatology images representing over 100 different skin conditions across a spectrum of skin tones measured by the FitzPatrick Skin Tone (FST) scale. For the purposes of this competition, a curated subset of ~4,500 images spanning 21 distinct conditions was provided to create a manageable, yet meaningful, classification problem while preserving the dataset's diversity and representational challenges.

- Train Data:
  - Includes labeled images of skin conditions, accompanied by metadata in train.csv. Images are organized into directories by label.
- Test Data:
  - Contains unlabeled images and metadata in test.csv, used for generating predictions for submission.
- Metadata Features:
  - md5hash: Unique identifier for each image.
  - label: Diagnosis or condition.
  - fitzpatrick_scale & fitzpatrick_centaur: Indicate skin tone.
  - ddi_scale: Severity rating.
  - Additional label partitions (nine_partition_label, three_partition_label) for various classification granularities.


**Data Preprocessing**

Key preprocessing steps included:
 - Appending File Paths:
     - Combined metadata with file directory paths to enable seamless image loading.
 - Label Encoding:
     - Converted categorical labels (skin condition names) into numerical form using label encoding, essential for model compatibility.
 - Train-Validation Split:
     - Performed an 80/20 split to divide the training set into training and validation subsets for robust performance evaluation.
 - Image Normalization & Augmentation:
     - Normalized image pixel values using rescaling (1./255).
     - Employed ImageDataGenerator to apply:
        - Rotation
        - Width and height shift
        - Horizontal flipping
     - This real-time data augmentation strategy helps to mitigate overfitting and enhance model generalization.
     

---

## Model Development  🔧
We initially experimented with various pre-trained models, including DenseNet201, InceptionV3, MobileNetV1 and V3, ResNet, and EfficientNet. Among them, InceptionV3 demonstrated the best out-of-the-box performance. Following this, our focus shifted primarily to testing different data augmentations (rotations, hues, brightness, etc.) with varying probabilities of application. Data augmentation provided to be the most useful at getting our score, for example, we created functions that created cutouts and noise injections within the images, which prevents the model from overfitting and helped us reach our final score

We also explored modifications at the architectural level, such as incorporating dropout to help regularize the model by preventing neurons from co-adapting too strongly. As we encountered increasing issues with overfitting, we expanded our model selection and experimented with different activation functions. Additionally, we reviewed recent machine learning research in dermatology to replicate useful methodologies—though not exactly, as many papers are tailored to specific skin conditions and do not always address our particular challenges.

One of the significant challenges we faced was the limited computational resources available on Colab. For instance, we attempted to generate synthetic images using SMOTE and GANs, but Colab's constraints prevented us from executing these techniques effectively.


---

## Results & Key Findings 🔑
![image](https://github.com/user-attachments/assets/ca078973-f30f-4dd3-a6a2-f7c83b493137)
We ended up getting a 0.44 accuracy score when submitting to the leaderboard which calculcates our model's accuracy using 70% of the test data. Our model's evaulation metrics were computing the training accuracy, validation accuracy, training loss, and validation loss. 

The DenseNet201 model was only able to get an accuracy of 7.5%, MobileNetV1 was able to get an accuracy score of 9.5%, and InceptionV3 was able to get a higher accuracy of 25% which is why we chose to continue with InceptionV3. We then implemented different data augmentation techniques listed above to boost our accuracy with InceptionV3. 

## Impact Narrative 🌍
- How project findings contribute to solving the real-world problem  
- Potential applications beyond the competition  
- Ethical considerations and broader implications  

---

## Next Steps & Future Improvements 🚀
## 🎯 Possible Improvements for Better Model Performance
Enhancing data augmentation with techniques like brightness adjustment, contrast normalization, and GAN-based synthetic data generation can improve model robustness. Fine-tuning pretrained models such as EfficientNet, ConvNeXt, and Vision Transformers may enhance classification accuracy. Addressing class imbalance using weighted loss functions, oversampling, or synthetic data generation ensures better performance across diverse skin tones. Employing ensemble learning by combining CNNs, transformers, and hybrid models can further improve predictions. Additionally, leveraging explainability and fairness tools like SHAP, LIME, and Fairlearn will help analyze model decision-making and reduce biases.

## 🔍 Additional Data Sources or Techniques to Explore

Incorporating diverse dermatology datasets such as Fitzpatrick17k, ISIC, and HAM10000 will enrich the model’s understanding of different skin conditions. Domain adaptation techniques using general medical image datasets can improve performance in dermatology-specific cases. Self-supervised learning approaches like SimCLR or MoCo can pretrain models on unlabeled skin images before fine-tuning. Crowdsourcing dermatologists or AI-assisted tools for refining labels can enhance data accuracy and model reliability.

## 🗺️ Steps for Future Project Development

Continuous benchmarking of model performance by tracking F1 scores across architectures and preprocessing pipelines is crucial. Detecting and mitigating biases by evaluating model predictions across demographic subgroups will ensure fairness. Deploying the model in real-world applications, such as an API or mobile-friendly app, will allow practical testing. Collaboration with AI fairness communities, dermatology experts, and developers can refine the model and improve transparency. Establishing a user feedback loop will help validate predictions, gather insights, and iteratively refine the model to enhance accuracy and fairness.


---
