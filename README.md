# Leveraging Large Language Models for Code-Mixed Data Augmentation in Sentiment Analysis
This repository contains datasets accompanying our paper [Leveraging Large Language Models for Code-Mixed Data Augmentation in Sentiment Analysis](https://aclanthology.org/2024.sicon-1.6/) (EMNLP '24). The datasets include both natural and synthetic data in Malayalam-English and Spanish-English.

## Datasets Overview

Each CSV file contains two columns:
- **Sentence**: This column includes the text of the sentences being analyzed. Each row represents a different sentence.
- **Label**: This column provides the sentiment label assigned to each sentence. The possible labels are:
  - **Positive**: Indicates a positive sentiment.
  - **Negative**: Indicates a negative sentiment.
  - **Neutral**: Indicates a neutral sentiment.

### Malayalam-English
The following files contain data for Malayalam-English code-mixing:

- **enma_natural_dev.csv**: Development set for natural Malayalam-English code-mixing data.
- **enma_natural_test.csv**: Test set for natural Malayalam-English code-mixing data.
- **enma_natural_train.csv**: Training set for natural Malayalam-English code-mixing data.
- **enma_synthetic_llm-generated.csv**: Synthetic data generated using language models for Malayalam-English code-mixing.

### Spanish-English
The following files contain data for Spanish-English code-mixing:

- **ensp_natural_dev.csv**: Development set for natural Spanish-English code-mixing data.
- **ensp_natural_test.csv**: Test set for natural Spanish-English code-mixing data.
- **ensp_natural_train.csv**: Training set for natural Spanish-English code-mixing data.
- **ensp_synthetic_llm-generated.csv**: Synthetic data generated using language models for Spanish-English code-mixing.
- **ensp_synthetic_randomly-translated.csv**: Synthetic data created through random translation techniques for Spanish-English code-mixing.
  
## Usage
You can load the datasets using `pandas` as follows:

```python
import pandas as pd

# Load Malayalam-English datasets
enma_train = pd.read_csv('path/to/enma_natural_train.csv')
enma_dev = pd.read_csv('path/to/enma_natural_dev.csv')
enma_test = pd.read_csv('path/to/enma_natural_test.csv')
enma_synthetic = pd.read_csv('path/to/enma_synthetic_llm-generated.csv')

# Load Spanish-English datasets
ensp_train = pd.read_csv('path/to/ensp_natural_train.csv')
ensp_dev = pd.read_csv('path/to/ensp_natural_dev.csv')
ensp_test = pd.read_csv('path/to/ensp_natural_test.csv')
ensp_synthetic_llm = pd.read_csv('path/to/ensp_synthetic_llm-generated.csv')
ensp_synthetic_random = pd.read_csv('path/to/ensp_synthetic_randomly-translated.csv')
```
## Coming Soon
The code and models used for data generation and processing will be released soon. Stay tuned for updates!

## Acknowledgments
We acknowledge the contributions of authors of the following papers, whose datasets we build upon:

- Gustavo Aguilar, Sudipta Kar, and Thamar Solorio. 2020. [LinCE: A Centralized Benchmark for Linguistic Code-switching Evaluation.](https://aclanthology.org/2020.lrec-1.223/) In *Proceedings of the Twelfth Language Resources and Evaluation Conference*, pages 1803–1813, Marseille, France. European Language Resources Association.
- Bharathi Raja Chakravarthi, Navya Jose, Shardul Suryawanshi, Elizabeth Sherly, and John Philip McCrae. 2020. [A Sentiment Analysis Dataset for Code-Mixed Malayalam-English.](https://aclanthology.org/2020.sltu-1.25/) In *Proceedings of the 1st Joint Workshop on Spoken Language Technologies for Under-resourced languages (SLTU) and Collaboration and Computing for Under-Resourced Languages (CCURL)*, pages 177–184, Marseille, France. European Language Resources association.
- Parth Patwa, Gustavo Aguilar, Sudipta Kar, Suraj Pandey, Srinivas PYKL, Björn Gambäck, Tanmoy Chakraborty, Thamar Solorio, and Amitava Das. 2020. [SemEval-2020 Task 9: Overview of Sentiment Analysis of Code-Mixed Tweets.](https://aclanthology.org/2020.semeval-1.100/) In *Proceedings of the Fourteenth Workshop on Semantic Evaluation*, pages 774–790, Barcelona (online). International Committee for Computational Linguistics.
