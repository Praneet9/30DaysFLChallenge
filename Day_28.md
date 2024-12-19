# Notes: DeepSight – Mitigating Backdoor Attacks in Federated Learning

---

## Overview:
- **Federated Learning (FL)**:
  - Enables multiple clients to collaboratively train a neural network (NN) model on private data without revealing the data.
  - Vulnerable to **targeted poisoning attacks**:
    - Backdoors are injected into the model, causing misclassification of adversary-controlled inputs.

---

## Problem with Existing Countermeasures:
1. Inefficiency in mitigating backdoor attacks.
2. Often exclude **benign models** of clients with **deviating data distributions**.
3. Results in poor performance of the aggregated model for such clients.

---

## DeepSight: A Novel Defense Approach

### Key Features:
1. **DeepSight’s Filtering Scheme**:
   - **Classifier + Clustering-based Similarity Estimations**:
     - Identifies suspicious model updates.
     - Uses labels of individual and similar models to determine acceptance or rejection of updates.
   - Prevents benign models with deviating data distributions from being filtered out.
   - Improves aggregated model performance for benign clients.
   
2. **Threshold Exceedings Metric**:
   - Analyzes **parameter updates** in real-time during training to detect anomalies.

3. **Two-Layer Structure**:
   - **Layer 1**: Classification-based filtering:
     - Removes poisoned models with high backdoor attack impact.
   - **Layer 2**: Weight clipping enforcement:
     - Focuses on mitigating backdoor behavior in the training process.

---

## Evaluation Metrics:
- **Backdoor Accuracy (BA)**: Measures attack success rate.
- **Model Accuracy (MA)**: Evaluates overall model performance.
- **Precision (PRC)**: Indicates probability of an accepted model being benign.
- **Negative Predictive Value (NPV)**: Probability of a filtered model being truly poisoned.

---

## Results:
1. **Effectiveness**:
   - Outperforms state-of-the-art defense mechanisms.
   - Works for both IID and non-IID data distributions.
   - Successfully mitigates targeted poisoning attacks in diverse scenarios.

2. **Broad Applicability**:
   - Tested against:
     - **5 NLP backdoors**.
     - **12 NIDS backdoors**.
   - Not restricted to specific attack targets or applications.

---

## Applications:
- Federated learning scenarios with:
  - Diverse client data distributions.
  - Vulnerability to backdoor attacks (e.g., in NLP, NIDS, or other sensitive domains).

---

## Advantages of DeepSight:
1. Preserves performance for benign clients with deviating data.
2. Effective against a wide range of backdoor attack types.
3. Real-time parameter analysis ensures early detection and mitigation.

---

## Limitations Addressed:
- DeepSight minimizes the exclusion of benign models in FL.
- Improves overall model robustness while maintaining high accuracy.

---

## Final Thoughts:
DeepSight introduces an innovative combination of **deep-model inspection** and **weight clipping strategies** to tackle backdoor attacks in federated learning. Its two-layer approach, combined with real-time parameter monitoring, ensures both effective detection of malicious updates and inclusion of benign clients. The comprehensive evaluation demonstrates its superiority in handling poisoning attacks across varied scenarios.