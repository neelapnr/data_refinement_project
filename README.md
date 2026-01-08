# Projet Data Refinement — Café Sales

## 1️⃣ Contexte

Ce projet consiste à réaliser un **data refinement complet** sur un dataset brut des ventes d’un café (`cafe_sales_dirty.csv`). L’objectif est de **nettoyer et transformer les données** pour qu’elles soient exploitables, cohérentes et prêtes pour l’analyse ou la visualisation.

Le dataset brut contient volontairement :  
- Des **valeurs manquantes**  
- Des **doublons**  
- Des **erreurs de format** (ex : "ERROR")  
- Des **incohérences** (ex : totaux incorrects)  

## 2️⃣ Structure du projet

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


## 3️⃣ Étapes réalisées

1. **Exploration des données** (Notebook 1)  
   - Chargement du dataset brut  
   - Identification des problèmes : valeurs manquantes, doublons, erreurs et incohérences  

2. **Nettoyage des données** (Notebook 2)  
   - Standardisation des noms de colonnes  
   - Remplacement des valeurs incorrectes par `NaN` et suppression des doublons  
   - Conversion des colonnes numériques et dates  
   - Remplissage des valeurs manquantes (médiane pour les numériques, `"unknown"` pour les catégorielles)  
   - Création d’une colonne calculée `total_spent_calculated` pour vérifier la cohérence  

3. **Transformation et vérification** (Notebook 3)  
   - Vérification des statistiques et de la cohérence des données  
   - Sauvegarde du dataset nettoyé dans `DATA/PROCESSED/cafe_sales_clean.csv`  

## 4️⃣ Réflexion

- Chaque étape a été justifiée pour **ne pas perdre de données importantes** et signaler les valeurs manquantes.  
- Travailler sur le dataset brut permet de comprendre **l’importance du nettoyage et de la transformation**.  
- Le dataset final est maintenant **exploitable et cohérent** pour toute analyse future.

## 5️⃣ Exécution

1. Installer les dépendances :  
```bash
pip install -r REQUIREMENTS.TXT
