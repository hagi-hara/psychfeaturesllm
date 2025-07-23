# How well do large language models mirror human cognition of word concepts? A comparison of psychological ratings for early-acquired English words

## Code description

```bash
# code structure
.
├── llm
│   ├── word_features_in_LLMs_exp1.ipynb
│   ├── word_features_in_LLMs_exp2.ipynb
│   ├── dataset
│   │   ├── prompt_list.xlsx
│   │   ├── word_features_exp1.csv
│   │   ├── word_features_exp2.csv
│   ├── results_exp1
│   ├── results_exp2
├── analysis
│   ├── ...

```

### llm
This directory contains the code and dataset for calculating word features by large language models (LLMs).

After running the code (`word_features_in_LLMs_exp1.ipynb` and `word_features_in_LLMs_exp2.ipynb`), you will find the results in the `results_exp1` and `results_exp2` directories.
```bash
# main results files
llm/results_exp1/concatenated_results.csv

# additional results files (few-shot results)
llm/results_exp2/concatenated_results.csv  
```