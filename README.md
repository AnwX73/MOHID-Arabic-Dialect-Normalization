# مُوحِّد — MOHID

MOHID is an Arabic Dialect Normalization System developed for **Arabthon 2026 – Arabic Dialects Track**.

The system converts Arabic dialect text into **Modern Standard Arabic (MSA)** while preserving the original meaning and context.

### Supported Dialects
- Saudi Arabic
- Egyptian Arabic
- Levantine Arabic

### Example
**Input:**  
أبي أغير موعد الحجز

**Output:**  
أريد تغيير موعد الحجز.

## Model
MOHID is based on **UBC-NLP/AraT5v2-base-1024** and was fine-tuned in two stages:

1. Fine-tuning on external Saudi and Egyptian dialect-to-MSA data.
2. Continued fine-tuning on the team-created MOHID dataset.

Final trained model:  
https://drive.google.com/file/d/1yuxlgq3NNuNYgg36MJcz1hsCyRhyeNRr/view?usp=sharing

## MOHID Dataset
The team-created dataset contains:

- 450 dialect–MSA pairs
- 150 unique meanings
- 3 dialects
- 6 domains: Education, Shopping, Travel, Food, Technology, and Daily Life

The dataset was split by `meaning_id`:

- Train: 360 pairs
- Validation: 45 pairs
- Test: 45 pairs

## External Data
Stage 1 used external Arabic STS supporting data containing Saudi and Egyptian dialect-to-MSA pairs.

Source: PLOS ONE  
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0272991

The external dataset is not included as part of the team-created MOHID dataset.

## Results
- BLEU: 42.52
- chrF: 65.91
- Exact Match: 31.11%

## Files
- `code/MOHID_Training.ipynb`
- `code/MOHID_Interface_Demo.ipynb`
- `data/MOHID_Dataset.xlsx`

## Technologies
Python, PyTorch, Hugging Face Transformers, AraT5v2, Google Colab, Pandas, and ipywidgets.

## Future Work
Future improvements include adding more Arabic dialects, expanding the dataset, improving semantic preservation, and deploying MOHID as an API for Arabic AI applications.

## Acknowledgments
MOHID was developed as a team project for **Arabthon 2026**.
