# Drug review rating classification

[Final submission notebook](Family_Guys_Final_Submission.ipynb) contains the source cells for the full project. The folders contain runnable standalone sections.

| Directory | Contents |
|---|---|
| data | Original data cleaning notebook |
| baselines | Original ten-class LR, original unweighted four-class LR, and improved weighted four-class LR |
| models | Six weighted combinations of DPCNN or TextRCNN with FastText, SGNS or GloVe |
| visualization | Original EDA and model figures |

## Inputs and execution

Launch Jupyter in the repository root. Restart the kernel between sections. The notebooks require Python and dependencies such as PySpark (with Java), PyTorch, pandas, NumPy, SciPy, scikit-learn, NLTK, matplotlib, seaborn, wordcloud and tqdm.

1. To run the original cleaning notebook, place `drugsComTrain_raw.csv` in the root. To run the weighted baseline and advanced models, restore the archived `data_64_16_20/` directory with `train.jsonl`, `validation.jsonl`, `test.jsonl`, and `manifest.json`.
2. For the original ten-class baseline, put the archived `clean_data.csv` in the root. Restore `split_manifest.csv` under `baseline_results/rating_teammate_policy_20261106_155015_111148/`.
3. For the historical four-class baseline, restore `feature_metadata.json`, `idf_values.npz`, `review_only_reg_0p1_parameters.npz` and `rating_model_comparison.csv` in that same directory. These reproduce the original features and validation set.
4. Check the original visualization's manually entered metrics against the final report and provide the real data before regenerating figures. Some metrics differ, and missing data can trigger a simulated fallback.

Keep raw data, archives, model weights and outputs outside Git.
