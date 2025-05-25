# Entangled Learning 2.2 — Alternating Teacher-Student

This project demonstrates a novel training method where two neural networks, trained on different views of the same data (original vs PCA), alternate their roles as teacher and student across training epochs.

## Features
- Breast cancer dataset (real-world)
- Alternating teacher-student entanglement
- KL divergence based mutual alignment
- Dynamic entanglement coefficient λ
- ROC/AUC evaluation

## Files
- `entangled_2_2_notebook.ipynb`: Interactive training notebook
- `README.md`: This file
- `requirements.txt`: Dependencies

## Run
```bash
pip install -r requirements.txt
```
Then launch the notebook.

