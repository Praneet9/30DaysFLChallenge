# Notes on "Differential Privacy Meets Neural Network Pruning"

## Summary
- **Focus:** Solving scalability issues in applying differential privacy (DP) to deep neural network (DNN) training.
- **Challenge:** DP-SGD struggles to train moderately-sized neural networks with high privacy protection.
- **Proposed Solution:** Using dimensionality reduction techniques inspired by neural network pruning to improve DP-SGD’s scalability.
- **Key Techniques:** Two modes of parameter updates:
  1. **Parameter Freezing:** Pre-prune the network and update only the remaining parameters using DP-SGD, reducing the parameter space and improving efficiency.
  2. **Parameter Selection:** Select which parameters to update during training and update only those using DP-SGD.
- **Use of Public Data:** Helps with parameter freezing or selection without additional privacy loss, but effectiveness depends on the similarity between private and public data.
- **Experimental Findings:** Reducing parameter space enhances performance in differentially private training. Random selection performs just as well as magnitude-based selection for pruning.

## Key Points
1. **Challenge Addressed:** Making DP-SGD scalable for deep learning with high privacy guarantees.
2. **Techniques Used:**
   - **Parameter Freezing**: Removes some parameters beforehand to reduce dimensionality.
   - **Parameter Selection**: Dynamically selects parameters to update during training.
3. **Pruning Methods:** 
   - **Random Selection:** Selects parameters randomly.
   - **Magnitude-Based Selection:** Selects parameters based on their importance (magnitude).
4. **Results:** Both pruning methods work well, with no additional privacy loss, and random selection performs as effectively as magnitude-based selection.
5. **Leverage Public Data:** Public datasets can improve freezing/selection efficiency without compromising privacy.

## Conclusion
The paper introduces a novel approach for improving the scalability of DP-SGD in training DNNs. By integrating pruning techniques, the method reduces computational overhead and improves efficiency while maintaining strong privacy guarantees. Leveraging public data offers further improvements without sacrificing privacy, making this a promising direction for scalable and private deep learning.
