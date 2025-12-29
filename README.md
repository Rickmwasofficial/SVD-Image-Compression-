# SVD from Scratch: Image Compression and Dimensionality Reduction

I implemented the **Singular Value Decomposition (SVD)** algorithm from scratch using NumPy to explore how matrix decomposition can be used for dimensionality reduction and data compression.

### Implementation Overview

The core of this project is a manual implementation of the SVD recipe (). Instead of using a high-level library for the decomposition, I derived the components by:

1. Constructing a Symmetric Positive Definite (SPD) matrix from the input data ().
2. Using **Eigendecomposition** (`np.linalg.eigh`) to find the eigenvalues and eigenvectors.
3. Sorting these components by "energy" (eigenvalue magnitude) to identify the most significant patterns.
4. Deriving the left-singular vectors () by mapping the right-singular vectors () through the original transformation matrix.

### Effectiveness and Use Cases

This implementation demonstrates how SVD effectively "squashes" data by retaining only the highest-ranking singular values. This process is essential for:

* **Noise Reduction:** Filtering out the low-magnitude singular values that often represent random noise.
* **Feature Extraction:** Uncovering the "essence" or deeper patterns of a dataset while discarding redundant information.
* **Low-Rank Approximation:** Reducing the storage requirements and computational load of large matrices without losing their structural integrity.

### Key Learnings

Building this from the ground up highlighted the importance of numerical stability, such as handling floating-point noise with tiny/negative eigenvalues and ensuring proper vector alignment during matrix reconstruction. It serves as a practical reminder of how foundational linear algebra powers complex AI tasks like principal component analysis (PCA) and latent semantic indexing.
