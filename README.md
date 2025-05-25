# Entangled Learning 2.2 — Alternating Teacher-Student

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/madara88645/entangled-ai-ts2/blob/main/entangled_2_2_notebook.ipynb)

Entangled Learning 2.2 introduces a new training scheme in which two neural networks take turns teaching each other. While one model sees the original feature space, the other learns from a reduced representation (via PCA). The twist? Their roles alternate every epoch — teacher becomes student, student becomes teacher.

This setup mimics real-world collaborative learning, where participants share insights across different perspectives.

# Key ideas:

Alternating Roles: Unlike static distillation, both models teach and learn. This dynamic encourages richer representations and prevents overfitting to one "truth."

Asymmetric Inputs: The two models operate on different feature views (raw vs PCA). This forces them to align semantically, not syntactically.

Entangled Loss: Combines standard classification loss with KL divergence between output distributions. The KL component only applies to the student — but who the student is, changes with time.

Dynamic λ Coefficient: The influence of the teacher increases gradually, allowing early independence and late convergence.

# Research Context
This notebook extends prior experiments (Entangled 2.0, 2.1) and explores the effect of bidirectional, temporally dynamic output alignment on model generalization. It demonstrates that even weak models with limited input (like PCA-compressed features) can achieve high performance when given the opportunity to both teach and learn.

## Features

- Real-world breast cancer dataset
- Alternating teacher-student entanglement training
- KL divergence-based mutual alignment
- Dynamic entanglement coefficient (λ)
- ROC/AUC evaluation for model performance

## Getting Started

### Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/madara88645/entangled-ai-ts2.git
cd entangled-ai-ts2
pip install -r requirements.txt

