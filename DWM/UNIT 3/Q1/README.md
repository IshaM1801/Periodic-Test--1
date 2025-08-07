🧩 Basic Algorithm (Top-Down Greedy Approach) 1. Start at the Root:
• Begin with the entire training dataset at the root node.
• All attributes and examples are available for consideration. 2. Select the Best Attribute:
• Choose an attribute to split the data using a heuristic or statistical measure, such as:
• Information Gain (ID3)
• Gain Ratio (C4.5)
• Gini Index (CART)
• This is a greedy step—the algorithm always selects the best attribute for the current split without backtracking. 3. Partition the Dataset:
• Split the training data into subsets based on the selected attribute’s values.
• Create a new branch for each possible value of that attribute. 4. Recurse:
• For each subset created in the previous step:
• If it is pure (i.e., all instances belong to the same class), create a leaf node with that class label.
• Otherwise, repeat the process (i.e., go back to step 2) with the subset.

⸻

✅ Conditions to Stop Splitting

Partitioning stops when one of the following conditions is met: 1. All samples at a node belong to the same class
→ Mark it as a leaf node with that class. 2. No more attributes to split on
→ Use majority voting (choose the class with the most instances) for classification at the leaf. 3. No more examples left for a branch
→ Use majority class from the parent node to assign the class label.

⸻

📦 Handling Continuous-Valued Attributes
• Continuous attributes must be discretized before or during tree construction.
• This involves finding optimal thresholds (e.g., age ≤ 30, income > $50k) to convert continuous data into binary splits.

⸻

🔁 Recursive Nature

The algorithm applies the same logic at each internal node, creating a divide-and-conquer structure until all branches terminate at leaf nodes.

Example given in next image
