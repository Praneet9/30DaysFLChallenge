# Udacity Course on Secure and Private AI

- **Global Differential Privacy**  
  - Adds noise to data/outputs before sharing to ensure privacy.  
  - Relies on a centralized trusted curator to manage the data and noise.  
  - Used to release aggregated statistics (e.g., census data) without exposing individual records.  
  - Balances privacy and utility using a privacy budget (ε), where smaller ε provides stronger privacy but less accurate results.  

- **Differential Privacy for Deep Learning**  
  - Protects individual data points by adding noise to gradient updates during training.  
  - Ensures that any single record has a negligible impact on the model’s output, reducing the risk of sensitive data leakage.  
  - Helps mitigate attacks like membership inference, where an adversary might deduce if a record was in the training data.  
  - **Example**: In healthcare, a deep learning model trained on patient data (e.g., predicting heart disease) can use differential privacy. Noise ensures no patient’s specific information can be extracted from the model, even with extensive queries, protecting patient confidentiality while enabling medical research.  

- **PATE (Private Aggregation of Teacher Ensembles)**  
  - Uses multiple teacher models trained on private datasets; a student model learns from noisy aggregated teacher outputs.  
  - Teachers answer queries through a noisy voting mechanism, ensuring individual teacher data remains private.  
  - Effective for distributed datasets (e.g., across multiple hospitals or schools) requiring collaboration without direct data sharing.  
  - Strong privacy guarantees due to noise in the voting process, making it robust against data leakage.  
