# MeHate Benchmark

Benchmarking pre-trained transformer models for hate speech 
detection in Romanized Marathi-English code-mixed text.


## Dataset
L3Cube-MeHate from L3Cube-Pune.
Clone from: https://github.com/l3cube-pune/MarathiNLP

## Models Evaluated
- mBERT (bert-base-multilingual-cased)
- XLM-RoBERTa (xlm-roberta-base)
- MuRIL (google/muril-base-cased)
- MahaBERT (l3cube-pune/marathi-bert)
- MeRoBERTa (l3cube-pune/me-roberta)

## Results (Macro-F1, mean over 3 seeds)
| Model       | Macro-F1        | AUC-ROC         |
|-------------|-----------------|-----------------|
| mBERT       | 0.6485 ± 0.0040 | 0.7087 ± 0.0079 |
| XLM-RoBERTa | 0.6521 ± 0.0049 | 0.7092 ± 0.0113 |
| MuRIL       | 0.6629 ± 0.0112 | 0.7343 ± 0.0089 |
| MahaBERT    | 0.6500 ± 0.0037 | 0.6960 ± 0.0028 |
| MeRoBERTa   | 0.7807 ± 0.0082 | 0.8783 ± 0.0031 |

## Requirements
pip install -r requirements.txt

## Usage
1. Clone the dataset:
   git clone https://github.com/l3cube-pune/MarathiNLP.git

2. Install dependencies:
   pip install -r requirements.txt

3. Run evaluation:
   python mehate_meroberta_fast.py

## Hardware
Experiments run on NVIDIA T4 GPU (Kaggle).
