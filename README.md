# Projet_Apprentissage_Machine_Analyse_Exploratoire_des_donnees

## Objectif du projet 
Ce projet effectué dans le cadre du cours Apprentissage Machine, consiste à récupérer les données, à visualiser les données, à préparer les données pour les algorithmes de Machine Learning, appliquée à un cas réel d'e-commerce.

L'objectif métier est de:
__Prédire le revenu généré par de novueaux clients d'un site e-commerce__ et d'identifier le profil du "bon client".

Ce travail prépare les données pour l'entraînement d'un modèle prédictif dans le devoir suivant.

## Méthodologie suivie
Ce projet implémente les étapes suivantes:
1. Compréhension du problème métier
2. Compréhension des données
3. Préparation des données
  - Nettoyage des données
  - Traitement des valeurs manquantes
  - Détection et correction des outliers
  - Enrichissement des données
4. Construction d'un pipeline automatisé

## Jeu de données 

Nous avons utilisé le jeu de donnée _Customer.csv_ représentant chaque profil des clients. Les variables sont: 

 - age
 - pages
 - first_item_prize
 - gender
 - ReBuy
 - New_click
 - country
 - revenue (variable cible)

Nous avons utilisé le jeu de donnée _CountryPopulation.csv_ représentant les populations par pays, ces variables sont:

 - Country
 - population

Nous avons utilisé également le jeu de donnée _CountryGDP.csv_ représentant les PIB par pays, ces variables sont:

 - Country
 - GDP_inhab

## Nettoyage des données 🧹

### Détection des valeurs manquantes ✔
 - Implémentation d'un traitement automatique via:
   - `SimpleImputer`
   - Fonctions personnalisées
### Détection des données aberrantes (Outliers) ✔
Méthode utilisée:
 - Boîte à moustaches
 - Amplitude interquartile (IQR)

Un __transformateur personnalisé_ a été développé pour:

  - Détecter les valeurs extrêmes
  - Remplacement des valeurs extrêmes via interpolation basée sur les quartiles

## Enrichissement des données 🔄

Un transformateur personnalisé a été développé pour:
1. Nettoyer les datasets `CountryPopulation` et `CountryGDP`
2. Uniformiser la clé `country`
3. Effectuer une jointure paramétrable enrich_data(PIB=True)

## Pipeline global ⚙️
Un pipeline scikit-learn a été construit pour automatiser:

 - Le nettoyage des valeurs manquantes
 - Le traitement des outliers
 - L'enrichissement des données
 - La préapration finale des données

### Avantages de cette pratique 🎯
 - Reproductibilité
 - Réutilisable sur  le jeu de test
 - Automatisation complète
 - Bonne partique en ML industriel

## Technologies utilisées 🛠
 - Python
 - Pandas
 - NumPy
 - Matplotlib /Seaborn
 - Scikit-learn
 - JupyterLab

## Compétences développées 📈
 - Analyse exploratoire de données
 - Détection et traitement d'anomalies
 - Construction de transformateurs personnalisés
 - Création de pipeline ML
 - Jointures multi-sources


