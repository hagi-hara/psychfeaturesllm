# How well do large language models mirror human cognition of word concepts? A comparison of psychological ratings for early-acquired English words

## Code description

```bash
# code structure
.
├── llm
│   ├── word_features_in_LLMs_exp1.ipynb
│   ├── word_features_in_LLMs_exp2.ipynb
│   ├── word_features_in_sd.ipynb
│   ├── dataset
│   │   ├── prompt_list.xlsx
│   │   ├── word_features_exp1.csv
│   │   ├── word_features_exp2.csv
│   │   ├── word_features_exp1_with_sd.csv
│   ├── results_exp1
│   ├── results_exp2
│   ├── results_sd
├── inference_results
│   ├── results_exp1
│   ├── results_exp2
│   ├── results_sd
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

word_features_in_sd.ipynb  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hagi-hara/psychfeaturesllm/blob/main/llm/word_features_in_sd.ipynb)

After running the code (`word_features_in_LLMs_exp1.ipynb`, `word_features_in_LLMs_exp2.ipynb` and `word_features_in_sd.ipynb`), you will find the results in the `results_exp1`, `results_exp2` and `results_sd` directories.
```bash
# main results files
llm/results_exp1/concatenated_results.csv

# additional results files (few-shot results)
llm/results_exp2/concatenated_results.csv  

# additional results files (std results)
llm/results_sd/std.csv
llm/results_sd/std_mean.csv
llm/results_sd/std_cossim.csv
```

## inference_results
This directory contains the results of the LLMs for the word features that we calculated by running the code in the `llm` directory.

## analysis
This directory contains the code and dataset for analyzing the data based on the estimates calculated by LLMs using the files in `llm` directory.

## static lexical psychological features -- human norms
- **Concreteness** ([Brysbaert et al., 2014](https://doi.org/10.3758/s13428-013-0403-5)): The extent to which words are concrete, meaning that they are grounded in sensory and motor experiences versus abstract, relying primarily on linguistic representations. 
-	**Imageability** ([Cortese et al., 2004](https://doi.org/10.3758/BF03195585); [Schock et al., 2012](https://doi.org/10.3758/s13428-011-0162-0)): The extent to which words arouse a sensory experience (e.g., mental image or sound) quickly and easily. It is known that imageability correlates with concreteness.
-	**Bodily interactiveness** ([Muraki et al., 2022](https://doi.org/10.3758/s13428-022-01798-4); [Pexman et al., 2019](https://doi.org/10.3758/s13428-018-1171-z)): How easily the human body can interact with a referent of a word physically, which is called body-object interaction (BOI). There are two measures: Adult BOI and Child BOI. For instance, although “fire” is physically interactable, its Child BOI is low as fire is dangerous and so difficult for children to interact with bodily.
-	**Iconicity** ([Winter et al., 2023](https://doi.org/10.3758/s13428-023-02112-6)): The extent to which a word form (i.e., label) is perceived as similar to its meaning. High iconicity has high form-meaning similarity (e.g., “zigzag”), while low iconicity indicates that the relationship between word form and its meaning seems rather arbitrary (e.g., “menu”).
-	**Socialness** ([Diveica et al., 2022](https://doi.org/10.3758/s13428-022-01810-x)): The degree to which a word has social relevance, such as the social characteristic of a person or group (e.g., “police”), social role (e.g., “friend”), or social behavior or interaction (e.g., “share”).
-	**Babiness** ([Perry et al., 2015](https://doi.org/10.1371/journal.pone.0137147)): The degree to which a word is associated with infants. Highly-rated words include “cute,” “milk,” and “peekaboo.”
-	**Valence, Arousal, and Dominance** ([Warriner et al., 2013](https://doi.org/10.3758/s13428-012-0314-x)): The extent to which words invoke three different types of emotions. Valence is a rating of how happy or pleasant a word makes a person feel (e.g., “hug” or “love”). Arousal refers to the intensity of emotion provoked by a word (e.g., “hate” or “party”). Dominance indicates the degree to which a word makes a person feel in control or powerful, as opposed to submissive or weak (e.g., “smile” or “successful”).
-	**Sensorimotor strength** ([Lynott et al., 2020](https://doi.org/10.3758/s13428-019-01316-z)): The extent to which a word evokes sensorimotor strength across six perceptual modalities (Auditory, Gustatory, Haptic, Interoceptive, Olfactory, and Visual) and five action effectors (Foot/Leg, Hand/Arm, Head, Mouth, and Torso).

```
# References
- Brysbaert, M., Warriner, A. B., & Kuperman, V. (2014). Concreteness ratings for 40 thousand generally known English word lemmas. Behavior Research Methods, 46(3), 904–911.
- Cortese, M. J., & Fugett, A. (2004). Imageability ratings for 3,000 monosyllabic words. *Behavior Research Methods, Instruments, & Computers*, 36(3), 384–387.
- Schock, J., Cortese, M. J., & Khanna, M. M. (2012). Imageability estimates for 3,000 disyllabic words. Behavior Research Methods, 44(2), 374–379.
- Muraki, E. J., Siddiqui, I. A., & Pexman, P. M. (2022). Quantifying children’s sensorimotor experience: Child body–object interaction ratings for 3359 English words. Behavior Research Methods, 54(6), 2864–2877.
- Pexman, P. M., Muraki, E., Sidhu, D. M., Siakaluk, P. D., & Yap, M. J. (2019). Quantifying sensorimotor experience: Body–object interaction ratings for more than 9,000 English words. Behavior Research Methods, 51(2), 453–466.
- Winter, B., Lupyan, G., Perry, L. K., Dingemanse, M., & Perlman, M. (2023). Iconicity ratings for 14,000+ English words. Behavior Research Methods, 56, 1640-1655.
- Diveica, V., Pexman, P. M., & Binney, R. J. (2022). Quantifying social semantics: An inclusive definition of socialness and ratings for 8388 English words. Behavior Research Methods, 55(2), 461–473.
- Perry, L. K., Perlman, M., & Lupyan, G. (2015). Iconicity in English and Spanish and its relation to lexical category and age of acquisition. PLOS ONE, 10(9), e0137147.
- Warriner, A. B., Kuperman, V., & Brysbaert, M. (2013). Norms of valence, arousal, and dominance for 13,915 English lemmas. Behavior Research Methods, 45(4), 1191–1207.
- Lynott, D., Connell, L., Brysbaert, M., Brand, J., & Carney, J. (2020). The Lancaster Sensorimotor Norms: Multidimensional measures of perceptual and action strength for 40,000 English words. Behavior Research Methods, 52(3), 1271–1291.
```
