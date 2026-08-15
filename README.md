# Neural Network from Scratch — Generative AI Lab

**MIT Academy of Engineering, Alandi, Pune**
Department of CSE (AIML) · Course: Generative AI Lab · Class: T.Y. Tech

## Student Information
- Name: Rameshwar Sanap
- PRN Number: 202401110021
- Batch: A2
- Date of Submission: 15th August 2026

## Objective
Implement a feedforward neural network **entirely from scratch in Python**, using only `numpy` for the model itself — no TensorFlow, PyTorch, or Keras. The implementation covers the forward pass, backpropagation, and training via gradient descent.

## Dataset
[`sklearn.datasets.load_digits`](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html) — 1,797 samples of handwritten digits (0–9), each an 8×8 grayscale image (64 features). It ships inside scikit-learn (originally sourced from the UCI ML Repository's *Optical Recognition of Handwritten Digits* dataset), so no external download is required and the notebook runs fully offline.

> **Note:** This is not the full MNIST dataset (28×28 images, 70,000 samples) — it's a smaller, self-contained stand-in chosen so the notebook needs zero setup. If your submission requires MNIST specifically, the data-loading cell needs to be swapped for `fetch_openml('mnist_784')` or `keras.datasets.mnist`.

## Architecture
| Layer  | Size | Activation |
|--------|------|------------|
| Input  | 64   | —          |
| Hidden | 64   | ReLU       |
| Output | 10   | Softmax    |

- **Loss function:** Categorical Cross-Entropy
- **Optimizer:** Batch Gradient Descent (manually implemented, no autograd)
- **Weight init:** He initialization for the ReLU hidden layer; small random init for the output layer
- **Hyperparameters:** learning rate `0.5`, `800` epochs, full-batch updates

## Files
| File | Description |
|------|-------------|
| `NeuralNetwork_FromScratch.ipynb` | Full notebook — data loading, from-scratch NN implementation, training, evaluation, visualizations.
| `README.md` | Atharva_Kadam_NeuralNetwork_FromScratch.ipynb |

## How to Run
1. Open `NeuralNetwork_FromScratch.ipynb` in Google Colab or Jupyter.
2. Run all cells top to bottom (`Runtime > Run all` in Colab). No external downloads or GPU needed — the whole notebook runs on CPU in under a minute.
3. Results are deterministic (`np.random.seed(42)`), so re-running reproduces the same numbers.

## Results
- **Final test accuracy:** ~96.4%
- **Final test loss:** ~0.09 (cross-entropy)
- Training/validation loss and accuracy curves, a confusion matrix, and sample predictions are all rendered inline in the notebook.

## Repository
GitHub Repository Link: https://github.com/atharva134kadam/gen-ai-ass1

## Declaration
I, Rameshwar Sanap, confirm that the work submitted in this assignment is my own and has been completed following academic integrity guidelines.
