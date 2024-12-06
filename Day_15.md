# Notes on "Can You Really Backdoor Federated Learning?"

## Summary
- **Federated Learning**: Decentralized approach where data remains on user devices instead of being centralized, improving privacy but introducing new vulnerabilities.
- **Backdoor Attacks**: Aim to degrade model performance on specific tasks while maintaining high performance on the main task.
- **Study Highlights**:
  - Includes non-malicious clients with correctly labeled data to mimic real-world settings.
  - Uses EMNIST dataset, which is user-partitioned and non-iid (non-independent and identically distributed), reflecting realistic data distributions.
- **Findings**:
  - Success of backdoor attacks depends on factors like the number of adversaries and the complexity of the targeted task.
  - Without robust defenses, backdoor attacks can severely affect model performance.
- **Defensive Strategies**:
  - Techniques like **norm clipping** and **"weak" differential privacy** effectively mitigate attacks while preserving model utility.
  - Leveraging public frameworks like TensorFlow Federated (TFF) makes experiments and replication easier.
- **Open-Source Contribution**: Authors have shared their implementation to encourage further research on backdoor defenses and attack strategies.

## Key Points
1. **Challenge**: Detecting and defending against adversarial backdoor attacks in federated learning.
2. **Attack Characteristics**:
   - Target specific tasks without affecting the overall performance.
   - Success depends on adversary proportion and task difficulty.
3. **Dataset**: EMNIST, which closely mirrors real-world, user-partitioned data.
4. **Defensive Techniques**:
   - **Norm Clipping**: Limits the size of gradients during training for added robustness.
   - **Weak Differential Privacy**: Ensures privacy while mitigating backdoor risks without degrading overall model quality.
5. **Framework**: Implemented using TensorFlow Federated (TFF) to facilitate replication and collaboration.
6. **Open Source**: Code is shared to encourage innovation in defense mechanisms and attack exploration.

## Conclusion
This study offers a detailed analysis of backdoor attacks in federated learning, emphasizing the need for robust defenses like norm clipping and weak differential privacy. By leveraging real-world datasets and open-sourcing their implementation, the authors provide a foundation for further advancements in securing federated learning systems against adversarial interventions.
