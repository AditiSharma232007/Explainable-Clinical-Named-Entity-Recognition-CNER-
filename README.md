# Explainable-Clinical-Named-Entity-Recognition-CNER-


##  Project Overview

This project implements a **Clinical Named Entity Recognition (CNER)** system using **ClinicalBERT**, enhanced with **Explainable AI (XAI)** techniques.
The goal is to identify medical entities (e.g., diseases, medications) from clinical text and provide **interpretable explanations** for model predictions.

---

##  Objectives

* Perform **Named Entity Recognition (NER)** on clinical text
* Use **ClinicalBERT** for contextual understanding
* Provide **model explainability** using:

  * Token importance (attention approximation)
  * Integrated Gradients (conceptual implementation)
  * Rule-based explanations
* Build a **hybrid explainable AI system**

---

##  Technologies Used

* Python
* PyTorch
* HuggingFace Transformers
* Datasets Library
* Captum (for explainability)
* Google Colab

---

##  Model Used

* **ClinicalBERT** (`emilyalsentzer/Bio_ClinicalBERT`)
* Fine-tuned for token classification (NER task)

---

##  Project Pipeline

1. **Data Preparation**

   * Custom clinical dataset created
   * Tokens and labels defined manually

2. **Tokenization**

   * Word-level tokenization using BERT tokenizer
   * Label alignment using `word_ids()`

3. **Model Training**

   * Fine-tuned ClinicalBERT using HuggingFace Trainer

4. **Prediction**

   * Token-level classification output

5. **Explainability Techniques**

   * **Attention (Simulated)**: Token importance using logits
   * **Integrated Gradients**: Implemented using Captum (conceptual due to runtime limits)
   * **Rule-Based System**: Keyword-based clinical interpretation

---

##  How to Run

1. Open Google Colab
2. Install dependencies:

   ```bash
   pip install transformers datasets seqeval captum
   ```
3. Run all cells in order
4. Execute the final pipeline:

   ```python
   full_pipeline("Patient has severe penicillin allergy and takes metformin 500mg")
   ```

---

##  Sample Output

* **NER Prediction**: Token-level classification
* **Attention Scores**: Importance of each token
* **Integrated Gradients**: Feature attribution (conceptual)
* **Rule-Based Output**: Clinical interpretation

---

##  Limitations

* Small custom dataset (not real clinical dataset)
* Integrated Gradients may not execute due to runtime constraints
* Attention is approximated due to backend limitations

---

##  Future Improvements

* Use real clinical datasets (e.g., MIMIC-III)
* Deploy as a web application
* Improve explainability with SHAP/LIME
* Optimize model performance

---

##  Conclusion

This project demonstrates how **transformer-based models** like ClinicalBERT can be combined with **Explainable AI techniques** to build transparent and reliable healthcare NLP systems.

---

##  Author

* Aaryan Sharma
* Aditi Sharma
* Suryakant Kumar
* Vashishth

---

##  Acknowledgment

* HuggingFace Transformers
* PyTorch
* Captum Library
