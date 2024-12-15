# Notes on "Federated Full-Parameter Tuning of Billion-Sized Language Models with Communication Cost under 18 Kilobytes"

## Summary
- **FedKSeed**: A novel approach proposed to fine-tune large language models (LLMs) using federated learning.
- **Key Problem**: 
  - Fine-tuning LLMs to improve natural language instruction responsiveness is essential.
  - Traditional federated fine-tuning relies on parameter-efficient methods, which underutilize full-parameter tuning's potential.
  - Full-parameter tuning in federated learning faces communication cost challenges.
- **Solution**:
  - FedKSeed drastically reduces communication costs using **zeroth-order optimization** with finite random seeds.
  - Enables federated full-parameter tuning of billion-sized LLMs directly on devices while preserving privacy.
  - Incorporates **probability-differentiated seed sampling** to prioritize impactful changes.

---

## Definitions
- **Fine-tuning**: Adjusting pre-trained models for specific tasks.
- **Federated Learning**: Training models across multiple devices without sharing raw data.
- **Optimization**: Improving a system’s performance through adjustments.
- **Communication Costs**: The data shared between devices during federated training.
- **Perturbations**: Minor adjustments made to a model during training.
- **Generalization**: The model's ability to perform well on unseen tasks.

---

## Key Points
1. **Motivation**:
   - Pre-trained LLMs need task-specific fine-tuning for optimal performance.
   - Full-parameter tuning can unlock greater performance but is impractical in federated settings due to high communication costs.

2. **FedKSeed Highlights**:
   - Leverages **zeroth-order optimization** to reduce transmission to only random seeds and scalar gradients (under 18 KB total).
   - Achieves **federated full-parameter tuning** while ensuring data privacy and usability on end devices.

3. **Innovations**:
   - **Probability-differentiated seed sampling**: Prioritizes impactful perturbations for efficient tuning.
   - Balances performance gains with minimal communication overhead.

4. **Experimental Results**:
   - Tested across six scenarios (various LLMs, datasets, and data partitions).
   - Demonstrates better **communication efficiency** and **task generalization** than existing methods.
   - Example: Achieved a **5% accuracy improvement** on sentiment analysis tasks (using BERT) while reducing communication costs by over 90%.

5. **Practical Implications**:
   - Enables on-device tuning of billion-sized models, respecting privacy constraints.
   - Suitable for applications with limited data or stringent privacy requirements.

---

## Conclusion
- **FedKSeed** represents a breakthrough in federated fine-tuning by making full-parameter tuning feasible for billion-sized LLMs.
- Balances privacy, communication efficiency, and task performance, making it ideal for real-world scenarios.
- Opens new doors for fine-tuning LLMs in privacy-sensitive and resource-constrained environments.
- The paper provides comprehensive experimental validation and open-source code for further research and practical applications.