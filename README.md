# Techniques for Enhanced Data Reconstruction and Analysis

This repository contains a collection of Python scripts dedicated to tackling complex data analysis problems through various advanced computational techniques. Each notebook is a distinct task, ranging from compressed sensing to image denoising using RKHS Ridge Regression.

## Compressed Sensing

- **Objective**: Recover an $s$-sparse vector $\textbf{x}$ from the output $\textbf{y = Ax}$, where $\textbf{A}$ is a $256 \times 512$ matrix.
- **Method**: Solve an $l_1$ minimization problem to find the sparsest $\textbf{x}$.
- **Experiment**: Conduct 20 independent experiments for sparsity levels ($s$) ranging from 1 to 128, evaluating the success rate of recovery.

## Smooth-Sparse Decomposition

- **Objective**: Decompose data into smooth and sparse components by minimizing a composite objective function that includes reconstruction error, smoothness penalty, and sparsity.
- **Tasks**:
  - Prove the convexity of the optimization problem.
  - Visualize smooth, sparse, and error components of data from a `data.mat` file.

## Matrix Recovery

- **Objective**: Reconstruct a low-rank $50 \times 50$ matrix, $M_0$, of rank 2, after randomly zeroing out 50% of its entries.
- **Method**: Solve an optimization problem minimizing the nuclear norm of $M$ while ensuring $M$ and $M_0$ match in non-zero entries.
- **Evaluation**: Compute the relative reconstruction error using the Frobenius norm between $M_0$ and the recovered $M$.

## RKHS Ridge Regression for Image Denoising

- **Objective**: Denoise an image from `peaks.mat` using RKHS Ridge Regression.
- **Procedure**:
  - Generate a 2D Gaussian kernel basis by the Kronecker product of two 1D Gaussian kernels.
  - Apply RKHS Ridge Regression to estimate pixel values.
  - Compute the smooth image and estimate noise standard deviation; visualize the result.
