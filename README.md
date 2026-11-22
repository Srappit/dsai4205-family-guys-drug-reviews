# Drug review rating classification

[Final submission notebook](Family_Guys_Final_Submission.ipynb) contains the source cells for the full project. The folders contain standalone notebooks.

## Best reported model results

The four-class results below are from Section 7 of the final report. All metrics are percentages.

| Model | Text representation | Accuracy | Macro Precision | Macro Recall | Macro-F1 |
|---|---|---:|---:|---:|---:|
| Original four-class baseline | Unigram TF-IDF | 59.48 | 47.06 | 43.97 | 43.86 |
| Improved four-class baseline | Bigram TF-IDF | 58.50 | 47.75 | 47.18 | 47.33 |
| DPCNN | FastText | **64.85** | **54.80** | 53.59 | **53.93** |
| DPCNN | SGNS | 62.71 | 53.24 | 52.36 | 52.72 |
| DPCNN | GloVe | 62.52 | 52.79 | 52.36 | 52.29 |
| TextRCNN | FastText | 62.45 | 52.51 | **53.89** | 52.85 |
| TextRCNN | SGNS | 62.83 | 53.55 | 53.22 | 53.36 |
| TextRCNN | GloVe | 59.69 | 51.81 | 50.83 | 51.11 |

The original four-class baseline was evaluated on validation data, and the improved baseline was evaluated on test data. The improved baseline's bigram configuration follows the implementation and Section 6 of the report.

The original **ten-class** baseline, which predicted exact ratings from 1 to 10, achieved **38.62% test accuracy** and **17.13% F1** (Section 3 of the report).

## Repository contents

| Directory | Contents |
|---|---|
| data | Original data cleaning notebook |
| baselines | Original ten-class LR, original unweighted four-class LR, and improved weighted four-class LR |
| models | Six weighted combinations of DPCNN or TextRCNN with FastText, SGNS or GloVe |
| visualization | Original EDA and model figures |
