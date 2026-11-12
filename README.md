# Espeon – FDS Pokémon Battles Prediction 2026

Team **Espeon's team**: Zahra Rezaei, Murad Hasanov, Aleksander Kamiński.

Predicting whether Player 1 wins a Gen 2 OU Pokémon battle from Player 1's team,
Player 2's lead Pokémon and the first 30 turns (10,000 training and 5,000 test battles).

## Contents

| File | Description | CV | Public |
|---|---|---|---|
| `submitted1.ipynb` | Selected submission 1 – multimodal ensemble: CatBoost (depths 5–7), LightGBM and XGBoost, simplex-weighted blend | – | 0.69733 |
| `submitted2.ipynb` | Selected submission 2 – pure CatBoost ensemble (4 models, fixed weights) | – | 0.69733 |
| `submitted3.ipynb` | Selected submission 3 – unified CatBoost ensemble (3 models, fixed weights) | – | 0.69666 |
| `zahra_core_matchup_v2.ipynb` | Core features (112) + type-chart damage, matchup and categorical features; 2×CatBoost + logistic regression | 0.680 (5-fold) | 0.682 |
| `Pokemon_Battle_Prediction_report.pdf` | One-page report | | |

The 10-fold OOF accuracy printed in the three selected notebooks (~0.72) uses early stopping
on the validation folds, so it is optimistic and is not reported as CV here.

## How to run

The Kaggle notebook **Final_submission_Espeon** clones this repository and runs the three
selected pipelines, producing `submission_1.csv`, `submission_2.csv` and `submission_3.csv`.

1. Open the notebook on Kaggle with the competition data
   *FDS: Pokémon Battles Prediction 2026* attached.
2. Run all cells. The full run takes about 5 hours on Kaggle CPU.

The competition data is not included in this repository; it is available on the competition page.
Only the competition data and the supplied Gen 2 type chart are used.
