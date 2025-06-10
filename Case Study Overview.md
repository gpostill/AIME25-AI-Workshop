# 🏥 Case Study Overview 

Welcome to the case study repository for the **Introduction to AI in Healthcare Workshop**. This hands-on case study will guide you through the process of evaluating different types of AI models in a real-world clinical context. Note: for details on how to navidate to each file see the README.md file.

---

## 📖 Case Study Scenario

**Scenario:**  
You have been asked to develop a model that automates the ordering of the initial set of tests needed in the emergency department of your local hospital. It can be used for a range of medical conditions and will prompt the traige nurse and responsible physician depending on the information they input into the chart. The model also displays confidence level. The healthcare professional can then activate the ordering of subsequent tests. The AI system achieves **92% overall accuracy** in validation.

Your task is to explore the implications of different model architectures for this clinical setting, especially as it pertains to fairness, explainability, and generalizability.

---

## 🧠 Models to Explore

In this case study, we will compare and reflect on the following four hypothetical models:

### 🔹 Model A: Non-generative Model
**Design:**  
A traditional supervised learning model (e.g., random forest) trained on structured electronic health record (EHR) data including age, sex, vital signs, presenting complaint, and prior diagnoses.

**Validation:**  
- Internal validation with a random 20% test split  
- Model performance evaluated using accuracy, precision-recall, and subgroup analysis (by sex, age group, comorbidity count)  
- SHAP values used for feature importance

---

### 🔹 Model B: Non-generative, Image-based Model
**Design:**  
A convolutional neural network (CNN) trained solely on chest X-rays and abdominal ultrasounds to predict the next best diagnostic test. No structured or text data used.

**Validation:**  
- Validated on a separate imaging dataset from a neighboring hospital  
- Performance measured via top-1 accuracy and AUC  
- Visual saliency maps generated to support interpretability

---

### 🔹 Model C: Multimodal Model
**Design:**  
A deep learning model integrating structured EHR data, clinical imaging, and unstructured triage notes using a combination of CNNs, transformers, and tabular fusion layers.

**Validation:**  
- Stratified k-fold cross-validation (5-fold)  
- Tested on a synthetic external dataset simulating a rural emergency department population  
- Fairness metrics computed across race, income quintile, and first language

---

### 🔹 Model D: Generative Model
**Design:**  
A fine-tuned generative large language model (LLM) that reads triage notes and vitals and outputs a free-text test ordering plan.

**Validation:**  
- Evaluated using prompt-response pairs across 1000 diverse patient cases  
- Expert review panel assessed clinical appropriateness (blinded)  
- Audited for hallucination, test over-ordering, and subgroup reliability

---



![image](https://github.com/user-attachments/assets/f0d3f003-2ed3-45c5-9601-3960b5c23a49)

<img width="155" alt="image" src="https://github.com/user-attachments/assets/cc89a041-9007-4e3e-92e9-f2aebcc7c7e5" />


_Last updated: June 2025_
