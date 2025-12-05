# MavenMarket_PowerBI
Business Intelligence project built with the MavenMarket dataset (Kaggle). Includes data cleaning, data modeling, DAX, and Power BI dashboard.
# 📊 PROJET BUSINESS INTELLIGENCE : MAVEN MARKET RAPPORT

Ce projet est une analyse détaillée de la performance des transactions de Maven Market, réalisée sous **Power BI Desktop**. L'objectif est de mettre en place une solution BI complète (ETL, Modélisation, DAX) qui sert de rapport interactif pour l'aide à la décision.

---

## 📌 Aperçu du Résultat Final (Quick Look)

Voici le produit final, le tableau de bord principal qui inclut la filtration par pays et l'analyse de rentabilité :

![Aperçu du Dashboard Final](RESSOURCES/10_Final_Dashboard_Apercu.png)

---

## 🛠️ I. Préparation et Transformation des Données (Power Query / ETL)

Cette phase assure la qualité, la gestion des types de colonnes et la consolidation des données sources avant leur chargement.

### 1. Vue d'Ensemble des Données Brutes

Visualisation de la Table de Faits avant le nettoyage, montrant les premières statistiques de validité des colonnes (pourcentage de Valide/Erreur/Vide).
![Vue de la Table de Faits dans Power Query](RESSOURCES/21_PQ_Apercu_Donnees_Brutes.png)

### 2. Étapes de Nettoyage Appliquées

Détail des étapes de transformation appliquées (changement de types, renommage, gestion des dates, consolidation) dans Power Query pour garantir la qualité de la Table de Faits.
![Étapes Appliquées dans Power Query (Nettoyage)](RESSOURCES/23_PQ_Etapes_Appliquees.png)

***

## 🏗️ II. Modélisation des Données (Star Schema)

Le modèle est construit pour la rapidité d'exécution des requêtes et la flexibilité de l'analyse, en respectant le schéma en étoile.

### 3. Vue Relations du Modèle Final

Le Schéma en Étoile complet montrant la liaison entre les Tables de Faits (`Transaction Data`) et toutes les Tables de Dimensions (`Produits`, `Clients`, `Stores`, etc.) par des relations (1 à N).
![Vue Relations du Schéma en Étoile](RESSOURCES/31_Modele_Relations_Schema.png)

### 4. Focus sur les Tables de Faits et Dimensions

Détail de la Table de Fait centrale qui agrège les transactions, et des tables de dimensions qui fournissent le contexte d'analyse.
![Focus sur les Tables de Fait et Dimensions](RESSOURCES/33_Modele_Tables_Dimensions.png)

***

## 🧮 III. Calculs DAX et Indicateurs Clés (KPIs)

Définition des mesures complexes pour l'analyse financière (Marge, Bénéfice) et l'analyse temporelle (Année-à-Date).

### 5. Mesures de Rentabilité et Marge

Calculs cruciaux basés sur les colonnes de prix et de coût pour évaluer la marge brute du marché.
![Formule DAX de Mesure de Rentabilité](RESSOURCES/42_DAX_Mesure_Rentabilite.png)

### 6. Time Intelligence (Analyse Temporelle)

Utilisation des fonctions DAX avancées pour le calcul des indicateurs cumulatifs (comme le Revenu YTD) et l'analyse des tendances.
![Formule DAX de Time Intelligence (Revenu YTD)](RESSOURCES/43_DAX_TimeIntelligence.png)

***

## 📊 IV. Analyse et Interactivité du Rapport

Présentation des pages de rapport, des KPIs finaux et de la preuve de l'interactivité du tableau de bord.

### 7. Le Tableau de Bord Final Complet

Le rapport final intégrant tous les KPIs (Transactions, Bénéfices, Rendement) et les analyses géographiques (Carte) et temporelles.
![Tableau de Bord Final Complet (Version Finale)](RESSOURCES/51_Dashboard_Final_Complet.png)

### 8. Focus Visuel sur l'Interactivité (Analyse Active)

Mise en évidence de l'interactivité du rapport: un clic sur un segment (ex: un pays ou une catégorie) filtre dynamiquement le reste du tableau de bord (ex: l'évolution des revenus hebdomadaires).
![Focus sur l'Évolution ou Classement Interactif](RESSOURCES/52_Dashboard_Focus_Visuel_Interactif.png)

### 9. Exemple de Narratif des Données (Key Insights)

Les boîtes de narratif qui résument les découvertes clés (insights) fournies par l'analyse des données.
![Cartes de Narratif de Données Clés](RESSOURCES/53_Dashboard_Narrative_Insights.png)

