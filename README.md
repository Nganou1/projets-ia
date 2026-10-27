# Projets IA & Machine Learning

**Franck Nankeng** · Chef de projet Data & IA · [LinkedIn](https://www.linkedin.com/in/franck-nankeng-51b43b297/)

Quatre projets exécutés de bout en bout en Python. Chaque notebook part d'une question métier,
justifie ses choix par une mesure et se termine par des conclusions chiffrées et leurs limites.

| # | Projet | Ce qu'il démontre | Résultat clé |
|---|---|---|---|
| 01 | [Dépistage du diabète](notebooks/01_depistage_diabete_classification.ipynb) | Classification supervisée, pipeline sans fuite de données, réglage du seuil de décision | AUC 0,837 ; rappel porté de 70 % à 77 % pour un usage de dépistage |
| 02 | [Segmentation et ACP](notebooks/02_segmentation_kmeans_acp.ipynb) | K-Means, analyse en composantes principales, effet de la normalisation | 97,1 % → 96,8 % d'exactitude avec 40 variables au lieu de 64 |
| 03 | [Réseau dense contre CNN](notebooks/03_deep_learning_ann_vs_cnn.ipynb) | Deep learning (Keras), test de robustesse, augmentation de données | Sur images décalées d'un pixel : 48 % (dense), 71 % (CNN), 98 % (CNN augmenté) |
| 04 | [Process mining d'un cycle achats](notebooks/04_process_mining_audit_p2p.ipynb) | PM4Py, conformance checking, note d'audit | 618 commandes déviantes, 11,73 M€ exposés (données simulées) · [dépôt dédié](https://github.com/Nganou1/process-mining-achats) |

## English summary

Four end-to-end Python projects: diabetes screening with threshold tuning for recall, unsupervised
segmentation and PCA, a dense-vs-convolutional network robustness study, and process mining of a simulated
purchase-to-pay cycle with an audit memo. Each notebook starts from a business question and ends with measured conclusions and limits.

## Lancer les notebooks

```bash
python -m venv .venv && source .venv/bin/activate   # Windows : .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

Les notebooks 01 à 03 lisent leurs données dans `data/` ou les chargent depuis scikit-learn.
Le notebook 04 génère son propre journal d'événements simulé ; il nécessite Graphviz pour l'export des schémas.

## Données

- `data/diabetes.csv` : Pima Indians Diabetes Database (National Institute of Diabetes and Digestive and Kidney Diseases).
- `data/salaires.csv` : petit jeu pédagogique âge / salaire.
- Chiffres manuscrits : `sklearn.datasets.load_digits` (1 797 images de 8 × 8 pixels).

## Origine

Les projets 01 à 03 partent d'exercices du cours d'intelligence artificielle du Pr Mohamed Youssfi.
Je les ai restructurés et approfondis : questions métier, protocoles d'évaluation, expériences supplémentaires
(réglage du seuil, effet de l'échelle, test de robustesse, augmentation de données) et conclusions.
