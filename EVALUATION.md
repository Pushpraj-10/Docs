# Final Evaluation Results

> [!NOTE] 
> `CNN + BiLSTM` stopped at epoch 23 while `CNN + SimpleKAN` converged faster and stopped at epoch 11 due to early stopping.


## 2. Detailed Test Results (Intra & Inter Dataset)

These metrics evaluate the generalizability of the models trained on DAIC-WOZ across unseen datasets.

### Accuracy (%)

| Model | DAIC-WOZ (Intra) | Dataset-Depression (Inter) | EATD-Corpus (Inter) |
| :--- | :--- | :--- | :--- |
| **CNN + BiLSTM** | 74.88% | 50.51% | 80.25% |
| **CNN + SimpleKAN** | 82.01% | 66.54% | 64.24% |

### Macro F1 Score

> [!TIP]
> Since depression datasets are highly imbalanced, the **Macro F1 Score** is the most reliable metric for true performance.

| Model | DAIC-WOZ (Intra) | Dataset-Depression (Inter) | EATD-Corpus (Inter) |
| :--- | :--- | :--- | :--- |
| **CNN + BiLSTM** | 0.5129 | 0.3630 | 0.5163 |
| **CNN + SimpleKAN** | 0.5019 | 0.6548 | 0.4490 |

### Key Takeaways
* **CNN + SimpleKAN** demonstrates significantly superior zero-shot generalizability on the `Dataset-Depression` cross-dataset test compared to BiLSTM. 
* **CNN + BiLSTM** tends to overfit slightly to specific acoustic conditions, yielding poorer inter-dataset transferability in some cases but strong performance on similar acoustic structures (like EATD).
