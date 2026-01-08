# Projet Data Refinement — Café Sales

## Le Contexte

Ce projet consiste à réaliser un **data refinement complet** sur un dataset brut des ventes d’un café. L’objectif est de **nettoyer et transformer les données** pour qu’elles soient exploitables, cohérentes.

Le dataset brut contient volontairement :  
- Des **valeurs manquantes**  
- Des **doublons**  
- Des **erreurs de format** (ex : "ERROR")  
- Des **incohérences** (ex : totaux incorrects)  

## La Structure du projet

DATA-REFINEMENT-PROJECT/
│
├── DATA/
│ ├── RAW/ # Dataset brut
│ └── PROCESSED/ # Dataset nettoyé
│
├── NOTEBOOKS/
│ ├── 01_EXPLORATION.ipynb
│ ├── 02_CLEANING.ipynb
│ └── 03_TRANSFORMATION.ipynb
│
├── REPORTS/
│ └── RAPPORT.PDF
│
├── README.MD
└── REQUIREMENTS.TXT


## Les Étapes que j'ai réalisées

1. **Exploration des données** (dans le notebook 1)  
   - Chargement du dataset brut  
   - Identification des problèmes tels que les valeurs manquantes,les doublons, les erreurs et les incohérences  

2. **Nettoyage des données** (dans le notebook 2)  
   - Standardisation des noms de colonnes  
   - Remplacement des valeurs incorrectes par `NaN` et suppression des doublons  
   - Conversion des colonnes numériques et dates  
   - Remplissage des valeurs manquantes (médiane pour les numériques, `"unknown"` pour les catégorielles)  
   

3. **Transformation et vérification** (dans le notebook 3)
   - Création d’une colonne calculée `total_spent_calculated` pour vérifier la cohérence  
   - Vérification des statistiques et de la cohérence des données  
   - Sauvegarde du dataset nettoyé dans `DATA/PROCESSED/cafe_sales_clean.csv`  



## Exécution

1. Installer les dépendances :  
```bash
pip install -r REQUIREMENTS.TXT
