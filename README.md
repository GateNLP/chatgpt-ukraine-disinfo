# Lying Blindly: Bypassing ChatGPT's Safeguards to Generate Hard-to-Detect Disinformation Claims at Scale

## Experiment Code

### Environment

A conda environment is provided in `environment.yml`.

### `code/claimreview_subset.ipynb`

Run language detection on the ClaimReview data and subset to English claims and relevant columns.

### `code/claimreview_topics.ipynb`

Topic modelling on ClaimReview data, then saves claims related to the war in Ukraine.

### `code/fine_tune_roberta.ipynb`

Fine-tune and evaluate the RoBERTa model following [Uchendu et al. (2020)](https://aclanthology.org/2020.emnlp-main.673/)


## Data

### ChatGPT-Generated Data

The ChatGPT-generated data is available upon request. To use with the experiment code, place in the `data/` directory.

### `data/claimreview.csv`

The 282 human-authored claims related to the war in Ukraine that were extracted from ClaimReview. For each claim, the claim text (from the `claimReviewed` field) and URL of the fact check (from the `url` field) are included.

This subset is derived from the [ClaimReview markups feed](https://www.datacommons.org/factcheck/download). The compilation of this dataset is licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/). Each individual claim is under the license terms of the publisher of the fact check. Please cite the ClaimReview dataset as the original source of this data and the associated paper as the source for the subsetting.

## Additional Data and Statistics

### `annotation_instructions.md`

Instructions provided to human annotators for the human-AI claim classification task, and the classification form.

### `additional_data/topic_list.csv`

Complete list of topics extracted from the ClaimReview data.

### `additional_data/liwc-22_descriptive_stats.csv`

The mean and standard deviation of [LIWC-22](https://www.liwc.app/) statistics for each of the three datasets. This can be used to compare this data with the LIWC-22 statistics of other datasets, for example those provided in the [_LIWC-22 Descriptive Statistics and Norms_](https://www.liwc.app/help/psychometrics-manuals) spreadsheet.

### `additional_data/zerogpt-full-labels.csv`

Frequency of claims assigned to the 9 ZeroGPT labels and their assingments to a boolean label.
