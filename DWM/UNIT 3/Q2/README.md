📘 Basic Algorithm (Naive Bayes Classifier – Probabilistic Model)

1. Start with the Training Dataset
   • Each data sample has features X = (x_1, x_2, …, x_n) and a class label C_k.
   • Goal: Predict the class of a new instance based on feature values.

⸻

2. Calculate Prior Probabilities
   • Compute the prior probability for each class:
   P(C_k) = \frac{\text{Number of training samples in } C_k}{\text{Total number of samples}}

⸻

3. Compute Conditional Probabilities (Likelihood)
   • For each feature x_i, calculate the likelihood given a class:
   P(x_i | C_k)
   • For categorical features, use frequency counts.
   • For continuous features, assume Gaussian distribution and use:
   P(x_i | C_k) = \frac{1}{\sqrt{2\pi\sigma^2}} \cdot e^{-\frac{(x_i - \mu)^2}{2\sigma^2}}

⸻

4. Apply Naive Bayes Formula
   • Compute the posterior for each class using Bayes’ Theorem:
   P(C*k | X) \propto P(C_k) \cdot \prod*{i=1}^{n} P(x_i | C_k)
   • Ignore the denominator as it’s constant across classes.

⸻

5. Make the Final Classification
   • Choose the class with the maximum posterior probability:
   \text{Predicted Class} = \arg\max*{C_k} P(C_k) \cdot \prod*{i=1}^{n} P(x_i | C_k)

⸻

✅ Assumptions and Characteristics
• Naive Assumption: All features are conditionally independent given the class.
• Efficient: Works well with high-dimensional data (e.g., text classification).
• Limitations: Independence assumption may not hold true in all datasets.

⸻
