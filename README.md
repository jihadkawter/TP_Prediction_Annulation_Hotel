# TP_Hotel_Cancellation_Classification

Projet réorganisé selon les recommandations du professeur Hafed.

## Ordre d'exécution
1. `notebooks/01_collecte.ipynb`
2. `notebooks/02_eda.ipynb`
3. `notebooks/03_pretraitement.ipynb`
4. `notebooks/04_models.ipynb`
5. `notebooks/05_evaluation.ipynb`

## Structure
- `data/source` : fichier source compressé
- `data/raw` : copie brute produite par le notebook 1
- `data/processed` : données transformées produites par le notebook 3
- `models` : préprocesseur et modèles entraînés
- `reports/figures` : graphiques EDA et évaluation
- `reports/metrics` : tableau comparatif des modèles
- `archive` : notebook original avant réorganisation

## Git
Après chaque évolution importante : `git add`, `git commit`, puis `git push`.


## Extension PCA (Séance 14)

Le projet inclut maintenant une comparaison complète avant/après Analyse en Composantes Principales :

- PCA ajustée uniquement sur `X_train` pour éviter la fuite d’information ;
- nombre de composantes sélectionné automatiquement pour conserver au moins 95 % de la variance ;
- matrices `X_train_pca.npz` et `X_test_pca.npz` ;
- objet `models/pca_95_variance.joblib` ;
- tableaux de variance et poids des composantes ;
- graphiques de variance expliquée et cumulée ;
- modèles Logistic Regression, Decision Tree et Random Forest entraînés sur les versions originale et PCA ;
- comparaison des performances et des temps de calcul dans `05_evaluation.ipynb`.


## Révision finale conforme aux dernières consignes

Le projet conserve exactement cinq notebooks : collecte, EDA, prétraitement/PCA, modèles et évaluation. La PCA est intégrée au notebook 3, ses modèles comparatifs au notebook 4 et son évaluation au notebook 5. Les comparaisons incluent le nombre de prédicteurs, les temps de traitement et les métriques de classification avant/après PCA.
