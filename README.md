# Green & Fast 2026 — Eco-Delivery Prediction

**Equipe :** Nexa Data Science — M1 Data & IA
**Client :** Eco-Delivery (Naima, CEO)
**Objectif :** Prédire le temps de livraison pour optimiser le positionnement des coursiers

---

## Prérequis

```bash
pip install pandas numpy scikit-learn
```

## Lancer le pipeline

```bash
# Depuis la racine du projet
python pipeline_model.py
```

Le script effectue automatiquement :
1. Chargement du fichier `train.csv`
2. Nettoyage (valeurs aberrantes, espaces, formats)
3. Feature engineering (distance GPS, heure de commande, temps de préparation)
4. Entraînement de deux modèles baseline
5. Affichage des métriques MAE / RMSE

## Structure du projet

```
.
├── train.csv               # Dataset brut (Kaggle Food Delivery)
├── pipeline_model.py       # Pipeline complet + modèles baseline
├── README.md               # Ce fichier
└── agile/
    ├── backlog.md          # User Stories priorisées
    ├── definition_of_done.md
    └── kanban.md
```

## Résultats obtenus (Baseline Sprint 1)

| Modèle              | MAE (min) | RMSE (min) |
|---------------------|-----------|------------|
| Régression Linéaire | ~5.x      | ~6.x       |
| Random Forest       | ~4.x      | ~5.x       |

> Les valeurs exactes sont affichées à l'exécution.

## Features utilisées

| Feature               | Description                              |
|-----------------------|------------------------------------------|
| `distance_km`         | Distance GPS restaurant → client (Haversine) |
| `Road_traffic_density`| Densité du trafic (encodée)              |
| `Weatherconditions`   | Météo (encodée)                          |
| `order_hour`          | Heure de commande                        |
| `prep_time_min`       | Temps entre commande et prise en charge  |
| `multiple_deliveries` | Livraisons simultanées                   |
| `Delivery_person_Age` | Âge du livreur                           |
| `Delivery_person_Ratings` | Note du livreur                      |

## Dataset

Source : [Kaggle — Food Delivery Dataset](https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset?select=train.csv)
