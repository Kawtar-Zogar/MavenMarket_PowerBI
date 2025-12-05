# MavenMarket_PowerBI
Business Intelligence project built with the MavenMarket dataset (Kaggle). Includes data cleaning, data modeling, DAX, and Power BI dashboard.
# 📊 PROJET BUSINESS INTELLIGENCE : MAVEN MARKET RAPPORT

Ce projet est une analyse détaillée de la performance des transactions de Maven Market, réalisée sous **Power BI Desktop**. L'objectif est de mettre en place une solution BI complète (ETL, Modélisation, DAX) qui sert de rapport interactif pour l'aide à la décision.

---

## 📌 Aperçu du Résultat Final (Quick Look)

Voici le produit final, le tableau de bord principal qui inclut la filtration par pays et l'analyse de rentabilité :

![Aperçu du Dashboard Final](RESSOURCES/Dashboard%20Final%20Complet.png)

---

## 🛠️ I. Préparation et Transformation des Données (Power Query / ETL)

Cette phase assure la qualité, la gestion des types de colonnes et la consolidation des données sources avant leur chargement.

### 1. Vue d'Ensemble des Données Brutes

Visualisation de la Table de Faits avant le nettoyage, montrant les premières statistiques de validité des colonnes. (Basée sur l'image 'Focus Table de Fait').
![Vue de la Table de Faits dans Power Query](RESSOURCES/Focus%20Table%20de%20Fait.png)

### 2. Étapes de Nettoyage Appliquées

Détail des étapes de transformation appliquées (changement de types, renommage, gestion des dates, consolidation) dans Power Query pour garantir la qualité de la Table de Faits.
![Étapes Appliquées dans Power Query (Nettoyage)](RESSOURCES/Étapes%20Appliquées.png)

***

## 🏗️ II. Modélisation des Données (Star Schema)

Le modèle est construit pour la rapidité d'exécution des requêtes et la flexibilité de l'analyse, en respectant le schéma en étoile.

### 3. Vue Relations du Modèle Final

Le Schéma en Étoile complet montrant la liaison entre les Tables de Faits et toutes les Tables de Dimensions par des relations (1 à N).
![Vue Relations du Schéma en Étoile](RESSOURCES/Vue%20Relations%20(Schema).png)

### 4. Focus sur les Tables de Faits et Dimensions

Détail de la Table de Fait centrale qui agrège les transactions, et des tables de dimensions qui fournissent le contexte d'analyse.
![Focus sur les Tables de Fait et Dimensions](RESSOURCES/Focus%20Dimensions.png)

***

## 🧮 III. Calculs DAX et Indicateurs Clés (KPIs)

Définition des mesures complexes pour l'analyse financière (Marge, Bénéfice) et l'analyse temporelle (Année-à-Date).

### 5. Mesures L'Asassiya (Mesure Simple)

Calculs basés sur les transactions pour les totaux simples (ex: Total des Transactions, Revenu Total).
![Formule DAX de Mesure Simple](RESSOURCES/Mesure%20Simple.png)

### 6. Mesures L'Mout't'aw'ra (Mesure Avancée)

Calculs complexes pour les indicateurs clés de performance tels que la Marge bénéficiaire.
![Formule DAX de Mesure Avancée (Marge)](RESSOURCES/Mesure%20Avancée.png)

### 7. Time Intelligence (Analyse Temporelle)

Utilisation des fonctions DAX avancées pour le calcul des indicateurs cumulatifs (comme le Revenu YTD) et l'analyse des tendances.
![Formule DAX de Time Intelligence (Revenu YTD)](RESSOURCES/Mesure%20Time%20Intelligence.png)

***

## 📊 IV. Analyse et Interactivité du Rapport

Présentation des pages de rapport, des KPIs finaux et de la preuve de l'interactivité du tableau de bord.

### 8. Le Tableau de Bord Final (Complet)

Le rapport final intégrant tous les KPIs (Transactions, Bénéfices, Rendement) et les analyses géographiques et temporelles.
![Tableau de Bord Final Complet](RESSOURCES/Dashboard%20Final%20Complet.png)

### 9. Focus Visuel sur l'Interactivité (Analyse Active)

Mise en évidence de l'interactivité du rapport: un clic sur un segment (ex: un pays ou une catégorie) filtre dynamiquement le reste du tableau de bord.
![Focus sur l'Évolution ou Classement Interactif](RESSOURCES/Focus%20Visuel.png)


