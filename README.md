# Accident Risk Prediction

Prédiction du risque d'accident et explicabilité du modèle avec
**SHAP**.

## 📘 Description du projet

Ce projet utilise un modèle **Random Forest** pour prédire la
probabilité d'accident à partir de données routières, météorologiques et
de trafic.\
Il inclut aussi une analyse d'explicabilité détaillée permettant de
comprendre l'impact de chaque variable sur les prédictions.

------------------------------------------------------------------------

## 🧪 Description des données

  Variable            Description
  ------------------- -------------------
  road_type           Type de route
  traffic_density     Densité du trafic
  avg_speed           Vitesse moyenne
  weather_condition   Conditions météo
  num_lanes           Nombre de voies
  road_surface        État de la route
  lighting            Luminosité
  accident_risk       Cible (0--1)

------------------------------------------------------------------------

## ⚙️ Pipeline Machine Learning

            +-----------------------+
            |     train.csv         |
            +----------+------------+
                       |
                       v
            +-----------------------+
            | Nettoyage / NaN       |
            +-----------------------+
                       |
                       v
            +-----------------------+
            | Encodage One-Hot      |
            +-----------------------+
                       |
                       v
            +-----------------------+
            | Standardisation       |
            | (Scaler_Accident.pkl) |
            +-----------------------+
                       |
                       v
            +-----------------------+
            | RandomForestRegressor |
            +-----------------------+
                       |
                       v
            +-----------------------+
            |   Prédictions + SHAP  |
            +-----------------------+

------------------------------------------------------------------------

## 📄 Contenu du notebook

-   Chargement et préparation des données\
-   Nettoyage et traitement des valeurs manquantes\
-   Encodage des variables catégorielles\
-   Standardisation des données\
-   Entraînement d'un Random Forest\
-   Évaluation (R2, RMSE)\
-   Explicabilité SHAP (summary plot, waterfall)

------------------------------------------------------------------------

## 🔍 SHAP

Exemples produits : - `shap.summary_plot` pour importance globale\
- `shap.waterfall` pour explication individuelle

------------------------------------------------------------------------

## 📁 Structure du projet

📁 Accident_Risk_Prediction/
│── Accident_Risk_Prediction_Fixed.ipynb
│── dataset/
│ │── train.csv
│ │── test.csv
│── Scaler_Accident.pkl
│── requirements.txt
│── README.md
    
------------------------------------------------------------------------

## 📬 Auteur

Projet réalisé pour un système prédictif explicable de risque
d'accident.
