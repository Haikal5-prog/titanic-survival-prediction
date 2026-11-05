# Titanic Survival Prediction

Projek machine learning pertama saya: meramal sama ada penumpang Titanic survive atau tidak.

## Dataset
Dataset Titanic daripada library `seaborn` (891 penumpang).

## Langkah
1. Load dan terokai data (EDA)
2. Bersihkan data (isi umur kosong dengan median, buang kolum `deck`, one-hot encoding)
3. Split train/test (80/20, stratified)
4. Train dua model: Logistic Regression dan Random Forest
5. Nilai guna accuracy, precision, recall dan confusion matrix

## Keputusan
| Model | Accuracy |
|---|---|
| Logistic Regression | 81.5% |
| Random Forest | 79.8% |

## Insight
- Perempuan dan penumpang kelas 1 mempunyai kadar survive lebih tinggi.
- Logistic Regression sedikit mengatasi Random Forest, kemungkinan kerana dataset kecil dan corak utamanya mudah.
- Recall kelas "survive" (0.69) lebih rendah berbanding kelas "mati" (0.89); model lebih mudah terlepas penumpang yang survive.
- Random Forest menunjukkan `fare`, jantina dan umur sebagai feature paling berpengaruh. Feature importance cenderung memihak kepada feature berangka berterusan, dan `fare` berkorelasi dengan `pclass`.
- `alive` tidak dimasukkan sebagai feature untuk mengelakkan data leakage.

## Tools
Python, pandas, seaborn, matplotlib, scikit-learn (Google Colab)

## Cara run
Buka notebook di Google Colab dan run semua cell mengikut turutan.
