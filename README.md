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
├── inference_results
│   ├── results_exp1
│   ├── results_exp2
├── analysis
│   ├── llm_analysis.Rproj
│   ├── analysis_exp1_1.Rmd
│   ├── analysis_exp1_2.Rmd
│   ├── analysis_exp2_1.Rmd
│   ├── analysis_exp2_2.Rmd
│   ├── dataset
│   │   ├── exp1
│   │   │   ├── concatenated_results.csv
│   │   │   ├── ...
│   │   ├── exp2
│   │   │   ├── concatenated_results.csv
│   │   │   ├── wordlist_exp2.csv
│   │   │   ├── ...
│   ├── figures
│   │   ├── exp1
│   │   │   ├── AoA_All.png
│   │   │   ├── ...
│   │   ├── exp2
│   │   │   ├── Exp2_1_All.png
│   │   │   ├── ...
```

## llm
This directory contains the code and dataset for calculating word features by large language models (LLMs).


### Run in Google Colab or Jupyter Notebook:

Word_features_in_LLMs_exp1.ipynb  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hagi-hara/psychfeaturesllm/blob/main/llm/Word_features_in_LLMs_exp1.ipynb)

Word_features_in_LLMs_exp2.ipynb  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hagi-hara/psychfeaturesllm/blob/main/llm/Word_features_in_LLMs_exp2.ipynb)

After running the code (`word_features_in_LLMs_exp1.ipynb` and `word_features_in_LLMs_exp2.ipynb`), you will find the results in the `results_exp1` and `results_exp2` directories.
```bash
# main results files
llm/results_exp1/concatenated_results.csv

# additional results files (few-shot results)
llm/results_exp2/concatenated_results.csv  
```

## inference_results
This directory contains the results of the LLMs for the word features that we calculated by running the code in the `llm` directory.

## analysis
This directory contains the code and dataset for analyzing the data based on the estimates calculated by LLMs using the files in `llm` directory.
