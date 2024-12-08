# BengaliClinicalMT

Official repository for the paper **"Extrinsic Evaluation of Machine Translation Quality via Downstream Tasks for Low-Resource Bengali Clinical Texts"**. This repository contains datasets, preprocessing pipelines, translation models, and scripts for evaluating Bengali machine-translated clinical texts on downstream clinical tasks, including Mortality Prediction (MP) and Length of Stay Prediction (LOS).

---

## Repository Contents

- `LICENSE`: License file for the repository.
- `README.md`: Documentation and usage instructions.
- `balanced_translated_dataset.csv`: Translated Bengali dataset obtained from machine translation models.
- `balanced_translated_dataset_preprocessed.csv`: Preprocessed version of the translated Bengali dataset.
- `classification-ben-opus-with-preprocessing.ipynb`: Jupyter notebook for downstream task classification using BanglaBERT.
- `translation-opus-with-preprocessing.ipynb`: Jupyter notebook for preprocessing and translation of clinical texts using OPUS-MT.
- `requirements.txt`: Python dependencies for reproducing the experiments.

---

## Abstract

Low-resource languages face significant challenges in the development of NLP solutions, particularly in specialized domains like healthcare. This repository implements the experiments detailed in our paper, including extrinsic evaluation of machine-translated Bengali clinical texts. It demonstrates how translation quality influences the performance of Bengali clinical NLP models on downstream tasks. 

---

## Features

1. **Dataset Creation**: Contains translated Bengali clinical text datasets derived from MIMIC-III admission notes.
2. **Preprocessing Pipelines**: Implements robust preprocessing for noisy clinical texts.
3. **Machine Translation**: Uses multiple machine translation models (e.g., OPUS-MT, ChatGPT, BanglaNMT) for English-to-Bengali translation.
4. **Downstream Tasks**: Evaluates translations via real-world tasks such as:
   - Mortality Prediction (MP)
   - Length of Stay Prediction (LOS)
5. **Comparative Analysis**: Includes extrinsic evaluation and comparison with intrinsic metrics like BLEU.

---

## Setup and Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/junayed-hasan/BengaliClinicalMT
   cd BengaliClinicalMT
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the MIMIC-III database (requires appropriate credentials) and preprocess the admission notes using the provided scripts. Please see https://github.com/bvanaken/clinical-outcome-prediction for more details.

---

## Usage

### Translation and Preprocessing
Run the notebook for preprocessing and translation:
```bash
jupyter notebook translation-opus-with-preprocessing.ipynb
```

### Downstream Task Evaluation
Use the classification notebook to evaluate the performance of BanglaBERT on the translated and preprocessed dataset:
```bash
jupyter notebook classification-ben-opus-with-preprocessing.ipynb
```

---

## Datasets

- **balanced_translated_dataset.csv**: Bengali translations of English clinical texts.
- **balanced_translated_dataset_preprocessed.csv**: Preprocessed Bengali clinical text dataset, cleaned for downstream task evaluation.

---

## Results

We evaluate translation quality through:
- **Intrinsic Metric**: BLEU score
- **Extrinsic Metrics**: AUROC scores for MP and LOS tasks

The full results and analysis are available in the paper and notebooks.

---

## Reproducibility

To ensure reproducibility:
1. Use the preprocessing and translation scripts to generate the datasets.
2. Follow the notebooks for training and evaluation on downstream tasks.
3. All code and implementation details are provided in this repository.


---

## Contact

For questions, please contact:

**Mohammad Junayed Hasan**  
Master’s Student, Computer Science  
Johns Hopkins University  
Email: [junayedhasan100@gmail.com](mailto:junayedhasan100@gmail.com)  
GitHub: [junayed-hasan](https://github.com/junayed-hasan)

Here’s the license and copyright section to add at the end of your `README.md` file:

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Copyright

© 2024 Mohammad Junayed Hasan, Johns Hopkins University. All rights reserved.
