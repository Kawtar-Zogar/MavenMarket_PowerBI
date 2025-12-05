# MavenMarket_PowerBI
Business Intelligence project built with the MavenMarket dataset (Kaggle). Includes data cleaning, data modeling, DAX, and Power BI dashboard.
# 📊 PROJET BUSINESS INTELLIGENCE : MAVEN MARKET RAPPORT

Ce projet est une analyse détaillée de la performance des transactions de Maven Market, réalisée sous **Power BI Desktop**. L'objectif est de mettre en place une solution BI complète (ETL, Modélisation, DAX) qui sert de rapport interactif pour l'aide à la décision.

---

## 📌 Aperçu du Résultat Final (Quick Look)

Voici le produit final, le tableau de bord principal qui inclut la filtration par pays et l'analyse de rentabilité :

![Aperçu du Dashboard Final](Ressources/Dashboard%20Final%20Complet.png)

> **Rapport de Synthèse :** Ce tableau de bord intègre les KPIs de performance clés tels que le Revenu Total, le Bénéfice, la Marge Bénéficiaire et l'analyse des transactions par produit. Il sert de point de départ pour l'exploration des données.

---

## 🛠️ I. Préparation et Transformation des Données (Power Query / ETL)

Cette phase assure la qualité, la gestion des types de colonnes et la consolidation des données sources avant leur chargement.

### 1. Vue de l'Interface Power Query

L'interface de l'éditeur Power Query montrant la structure de travail.
![Vue de l'Interface Power Query](Ressources/Interface%20Power%20Query.png)

> **Rôle :** L'interface de l'éditeur Power Query est l'outil central pour l'importation, le nettoyage et la transformation de toutes les tables sources (Faits et Dimensions) avant le chargement dans le modèle.

### 2. Vue d'Ensemble des Données Brutes

Visualisation de la Table de Faits avant le nettoyage, montrant les premières statistiques de validité des colonnes.
![Vue de la Table de Faits dans Power Query](Ressources/Focus%20Table%20de%20Fait.png)

> **Nettoyage :** Cette vue confirme la nécessité d'opérations de nettoyage, notamment la gestion des valeurs manquantes ou incohérentes (erreurs) et l'ajustement des types de données pour les identifiants (IDs) et les valeurs numériques.

### 3. Étapes de Nettoyage Appliquées

Détail des étapes de transformation appliquées (changement de types, renommage, gestion des dates, consolidation) dans Power Query pour garantir la qualité de la Table de Faits.
![Étapes Appliquées dans Power Query (Nettoyage)](Ressources/Étapes%20Appliquées.png)

> **Logique de Transformation :** Toutes les étapes de transformation sont enregistrées, de l'élimination des colonnes inutiles à la modification des types (`Date`, `Text`, `Nombre entier`) pour préparer les tables pour le Schéma en Étoile.

### 4. Fusion des Données

Détail de l'étape de fusion (Merge) ou de combinaison (Append) des différentes sources de données.
![Opération de Fusion des Données](Ressources/L'FusionCombinaison.png)

> **Intégration :** Cette étape montre comment différentes tables (ex: `Transactions` et `Retours`) ont été combinées ou fusionnées pour créer une table de faits complète ou pour enrichir les dimensions.

***

## 🏗️ II. Modélisation des Données (Star Schema)

Le modèle est construit pour la rapidité d'exécution des requêtes et la flexibilité de l'analyse, en respectant le schéma en étoile.

### 5. Vue Relations du Modèle Final

Le Schéma en Étoile complet montrant la liaison entre les Tables de Faits et toutes les Tables de Dimensions par des relations (1 à N).
![Vue Relations du Schéma en Étoile](Ressources/Vue%20Relations%20(Schema).png)

> **Schéma en Étoile :** Ce modèle utilise la table de faits centrale (`Transaction Data`) reliée à toutes les tables de dimensions (Clients, Produits, Stores, etc.) par des relations un-à-plusieurs (1 à N), garantissant l'intégrité et la performance des requêtes DAX.

### 6. Focus sur les Tables de Faits et Dimensions

Détail de la Table de Fait centrale qui agrège les transactions, et des tables de dimensions qui fournissent le contexte d'analyse.
![Focus sur les Tables de Fait et Dimensions](Ressources/Focus%20Dimensions.png)

> **Rôle du Modèle :** Confirmation que la modélisation sépare les données transactionnelles (les faits) des données descriptives (les dimensions), optimisant ainsi la navigation des filtres et des segments dans le rapport.

***

## 🧮 III. Calculs DAX et Indicateurs Clés (KPIs)

Définition des mesures complexes pour l'analyse financière (Marge, Bénéfice) et l'analyse temporelle (Année-à-Date).

### 7. Mesures Simples (Mesure Simple)

Calculs basés sur les transactions pour les totaux simples (ex: Total des Transactions, Revenu Total).
![Formule DAX de Mesure Simple](Ressources/Mesure%20Simple.png)

> **Agrégation de Base :** Ces mesures utilisent des fonctions DAX de base (`SUM`, `COUNTROWS`) pour créer les indicateurs primaires affichés sur les cartes du rapport.

### 8. Mesures Avancées (Mesure Avancée)

Calculs complexes pour les indicateurs clés de performance tels que la Marge bénéficiaire.
![Formule DAX de Mesure Avancée (Marge)](Ressources/Mesure%20Avancée.png)

> **Logique Métier :** Ces mesures incorporent la logique métier (calcul du bénéfice et de la marge) en utilisant `SUMX` ou `CALCULATE` pour manipuler les contextes de filtre et produire des ratios financiers précis.

### 9. Time Intelligence (Analyse Temporelle)

Utilisation des fonctions DAX avancées pour le calcul des indicateurs cumulatifs (comme le Revenu YTD) et l'analyse des tendances.
![Formule DAX de Time Intelligence (Revenu YTD)](Ressources/Time%20Intelligence.png)

> **Analyse Tendance :** La mesure de type "Year-To-Date" (Année à Date) utilise les fonctions de Time Intelligence (comme `TOTALYTD`) pour comparer les performances de la période en cours.

***

## 📊 IV. Analyse et Interactivité du Rapport

Présentation des pages de rapport, des KPIs finaux et de la preuve de l'interactivité du tableau de bord.

### 10. Le Tableau de Bord Final (Première Version)

Le rapport final intégrant tous les KPIs (Transactions, Bénéfices, Rendement) et les analyses géographiques et temporelles.
![Tableau de Bord Final (Première Version)](Ressources/Dashboard%20Final.png)

> **Conception :** Cette version initiale montre la disposition des visuels et la sélection des graphiques (cartes, graphiques à barres, treemap) avant l'application de la mise en forme et des couleurs finales.

### 11. Le Tableau de Bord Final (Version Complète)

Le rapport final après toutes les retouches visuelles, prêt à l'emploi.
![Tableau de Bord Final Complet](Ressources/Dashboard%20Final%20Complet.png)

> **Esthétique :** La version finale montre l'application de la charte graphique, les objectifs de performance (targets) sur les jauges et la mise en page soignée pour faciliter la lecture et la prise de décision.

### 12. Focus Visuel sur l'Interactivité (Analyse Active)

Mise en évidence de l'interactivité du rapport: un clic sur un segment (ex: un pays ou une catégorie) filtre dynamiquement le reste du tableau de bord.
![Focus sur l'Évolution ou Classement Interactif](Ressources/Focus%20Visuel.png)

> **Preuve d'Analyse :** Ce visuel démontre la fonctionnalité de filtrage (slicing) du rapport. Un clic sur une région ou une catégorie met à jour tous les autres graphiques (cartes, tendances), validant l'interconnexion du modèle.




