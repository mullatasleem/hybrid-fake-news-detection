# Full results (as reported in the paper)

All metrics: accuracy / precision / recall / F1-score. 80:20 stratified split.

## ISOT Fake News Dataset (44,919 articles)

### Individual models

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Logistic Regression | 0.9424 | 0.9275 | 0.9534 | 0.9403 |
| SVM | 0.9547 | 0.9470 | 0.9583 | 0.9526 |
| Random Forest | 0.9344 | 0.9301 | 0.9321 | 0.9311 |
| RNN | 0.9577 | 0.9500 | 0.9616 | 0.9558 |
| LSTM | 0.9586 | 0.9526 | 0.9607 | 0.9566 |
| GRU | 0.9576 | 0.9494 | 0.9621 | 0.9557 |

### Hybrid ensembles (soft voting)

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| RF + RNN | 0.9605 | 0.9524 | 0.9651 | 0.9587 |
| RF + LSTM | **0.9650** | — | — | — |
| RF + GRU | 0.9640 | — | — | — |
| LR + RNN | 0.9592 | 0.9514 | 0.9635 | 0.9574 |
| LR + LSTM | 0.9604 | 0.9545 | 0.9625 | 0.9585 |
| LR + GRU | 0.9597 | 0.9509 | 0.9651 | 0.9579 |
| SVM + RNN | 0.9620 | 0.9563 | 0.9642 | 0.9602 |
| SVM + LSTM | 0.9628 | 0.9577 | 0.9644 | 0.9610 |
| SVM + GRU | 0.9628 | 0.9556 | 0.9667 | 0.9611 |

### Padding fusion (pre + post)

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| LSTM pre+post | 0.9871 | 0.9826 | 0.9881 | 0.9865 |
| GRU pre+post | **0.9901** | 0.9911 | 0.9896 | 0.9904 |
| RNN pre+post | 0.9712 | 0.9680 | 0.9714 | 0.9697 |

## Fake_Real_News_Data (6,335 articles, Kaggle)

### Individual models

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Logistic Regression | 0.9100 | 0.9398 | 0.8781 | 0.9079 |
| SVM | 0.9313 | 0.9424 | 0.9203 | 0.9312 |
| Random Forest | 0.9013 | 0.9133 | 0.8891 | 0.9010 |
| RNN | 0.8706 | 0.8662 | 0.8797 | 0.8729 |
| LSTM | 0.8998 | 0.8834 | 0.9234 | 0.9030 |
| GRU | 0.8714 | 0.8756 | 0.8688 | 0.8722 |

### Hybrid ensembles (attention-based)

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| RF + AttRNN | 0.9092 | 0.9173 | 0.9016 | 0.9094 |
| RF + AttLSTM | 0.8942 | 0.9161 | 0.8703 | 0.8926 |
| RF + AttGRU | 0.9006 | 0.9066 | 0.8953 | 0.9009 |
| LR + AttRNN | 0.9084 | 0.9253 | 0.8906 | 0.9076 |
| LR + AttLSTM | 0.8950 | 0.9204 | 0.8672 | 0.8930 |
| LR + AttGRU | 0.8982 | 0.9088 | 0.8875 | 0.8980 |
| SVM + AttRNN | **0.9313** | 0.9410 | 0.9219 | 0.9313 |
| SVM + AttLSTM | 0.9148 | 0.9346 | 0.8938 | 0.9137 |
| SVM + AttGRU | 0.9171 | 0.9239 | 0.9109 | 0.9174 |

### Padding fusion (pre + post)

| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| LSTM pre+post | **0.9250** | 0.9150 | 0.9370 | 0.9260 |
| GRU pre+post | 0.8600 | 0.8920 | 0.8200 | 0.8550 |
| RNN pre+post | 0.7490 | 0.7440 | 0.7600 | 0.7520 |

*Source: Tables III–VI of the paper. Cells marked — were not legible in the source table extraction.*
