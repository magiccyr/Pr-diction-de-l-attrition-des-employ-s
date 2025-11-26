# 📌 Projet IA — HumanForYou

- Analyse et prédiction du turnover des employés

# 👥 Groupe 1

- Romain HEMART

- Cyr-Manuel DJOKI

- Antoine TAFFOUREAU

- Alban GODIER

📅 19/12/2024

# 🎯 Objectif du projet

L’entreprise pharmaceutique HumanForYou, basée en Inde, fait face à un turnover élevé. Le salarié type reste environ 500 jours, ce qui entraîne :

- des coûts de recrutement importants,

- une perte de productivité,

- un manque de stabilité pour l’entreprise.

L’objectif est de développer un modèle prédictif permettant d’identifier les employés susceptibles de quitter l’entreprise afin de :

- anticiper les départs,

- favoriser des actions RH ciblées,

- améliorer la rétention.

# 🗂️ Données utilisées

Le projet exploite deux sources principales :

## 1. Base RH générale

Comprend notamment :

- Age, Gender, Education, Department, JobRole

- DistanceFromHome

- MonthlyIncome, PercentSalaryHike

- TotalWorkingYears, YearsAtCompany

- WorkLifeBalance, JobSatisfaction...

- Attrition (variable cible)

## 2. Dernière évaluation managériale

- EmployeeID

- JobInvolvement

- PerformanceRating

## 3. Enquête sur la qualité du travail

- EnvironmentSatisfaction

- RelationshipSatisfaction

- WorkLifeBalance

JobSatisfaction

# 🧹 Préparation des données

Le notebook inclut :
- Nettoyage des valeurs manquantes
- Encodage des variables catégorielles
- Analyse exploratoire (corrélations, distributions, métriques RH)
- Fusion des différentes sources de données
- Gestion des déséquilibres de classes (turnover = 16%)

# 📊 Analyse exploratoire (EDA)

Les points clés identifiés :

- Les employés jeunes, peu expérimentés ou habitant loin ont plus tendance à partir.

- Les scores faibles de satisfaction et de balance vie pro / vie perso sont corrélés à l’attrition.

- Le salaire n’est pas un facteur déterminant isolé.

- Certaines features sont très discriminantes : OverTime, JobRole, EnvironmentSatisfaction, YearsAtCompany.

# 🤖 Modélisation

Plusieurs modèles ont été testés dans le notebook :

- Logistic Regression

- Random Forest

- XGBoost

- Decision Tree

- KNN

- SVM

Chaque modèle a été évalué via :

- Accuracy

- F1-score

- Recall (critique pour ne pas manquer les employés à risque)

- Matrice de confusion

# 🏆 Résultats

Le XGBoost et la Random Forest se distinguent grâce à :

- Un bon compromis Recall / Précision

- Une forte capacité à capturer les non-linéarités

- Une meilleure gestion du déséquilibre de classes

Les variables les plus importantes selon les modèles :

- OverTime

- JobSatisfaction

- EnvironmentSatisfaction

- TotalWorkingYears

- YearsAtCompany

- WorkLifeBalance

# 📈 Visualisations incluses dans le notebook

- Histogrammes, boxplots, heatmaps

- Analyse des distributions par étiquette (Attrition vs Non-Attrition)

- Importance des variables

- Matrices de confusion

- Courbes ROC

# 📦 Technologies et librairies

- Python 3.x

- pandas, numpy

- matplotlib, seaborn

- scikit-learn

- xgboost

- imbalanced-learn

# 🚀 Améliorations possibles

- Optimisation hyperparamètres (GridSearchCV / Optuna)

- Intégration d’un tableau de bord (Streamlit)

- Création d’un pipeline déployable

- Analyse coût-bénéfice RH (fausses alertes vs. départs manqués)
