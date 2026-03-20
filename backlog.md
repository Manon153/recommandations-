# Backlog Priorisé — Green & Fast 2026

> Méthode : MoSCoW (Must / Should / Could / Won't)
> Sprint duration : 2 semaines

---

## EPIC 1 — Pipeline de données

### US-01 ★★★ MUST
**En tant que** Data Scientist,
**je veux** charger et nettoyer le dataset brut,
**afin de** disposer d'une base de données fiable pour l'entraînement.

**Critères d'acceptation :**
- Suppression des espaces parasites dans toutes les colonnes
- Colonne `Time_taken(min)` convertie en entier
- `Weatherconditions` nettoyée du préfixe "conditions "
- Moins de 5% de valeurs manquantes résiduelles

**Estimation :** 3 points

---

### US-02 ★★★ MUST
**En tant que** Data Scientist,
**je veux** calculer la distance réelle restaurant→client via les coordonnées GPS,
**afin d'** avoir une feature déterminante pour la prédiction.

**Critères d'acceptation :**
- Formule Haversine implémentée et testée
- Distance en km ajoutée comme colonne `distance_km`
- Valeurs cohérentes (0.5–50 km pour une livraison urbaine)

**Estimation :** 2 points

---

### US-03 ★★☆ MUST
**En tant que** Data Scientist,
**je veux** encoder les variables catégorielles (météo, trafic, ville, type de commande),
**afin que** les modèles ML puissent les traiter.

**Critères d'acceptation :**
- Toutes les colonnes catégorielles encodées
- Pas de data leakage (LabelEncoder fit sur train uniquement)

**Estimation :** 2 points

---

## EPIC 2 — Modèle Baseline

### US-04 ★★★ MUST
**En tant que** CEO d'Eco-Delivery,
**je veux** un modèle capable de prédire le temps de livraison,
**afin de** pré-positionner mes coursiers avant les pics de commandes.

**Critères d'acceptation :**
- Au moins un modèle entraîné (Random Forest ou Régression Linéaire)
- MAE < 8 minutes sur le set de test
- Résultats reproductibles (`random_state=42`)

**Estimation :** 5 points

---

### US-05 ★★☆ SHOULD
**En tant que** Data Scientist,
**je veux** comparer deux modèles baseline,
**afin de** choisir la meilleure approche pour le Sprint 2.

**Critères d'acceptation :**
- Régression Linéaire et Random Forest comparés
- Tableau comparatif MAE / RMSE affiché
- Meilleur modèle identifié et justifié

**Estimation :** 3 points

---

### US-06 ★★☆ SHOULD
**En tant que** CEO,
**je veux** connaître les facteurs qui allongent le plus les livraisons,
**afin d'** orienter mes décisions opérationnelles.

**Critères d'acceptation :**
- Feature importances du Random Forest affichées
- Top 5 features commentées avec interprétation métier

**Estimation :** 2 points

---

## EPIC 3 — Organisation Agile

### US-07 ★★★ MUST
**En tant que** membre de l'équipe,
**je veux** un Kanban à jour avec l'historique des tâches,
**afin de** montrer notre organisation au client.

**Estimation :** 1 point

---

### US-08 ★★☆ SHOULD
**En tant que** présentateur,
**je veux** un README clair expliquant comment lancer le code,
**afin que** n'importe qui puisse reproduire les résultats.

**Estimation :** 1 point

---

## EPIC 4 — Sprint 2 (Futures itérations)

### US-09 ★☆☆ COULD
**En tant que** CEO,
**je veux** un dashboard simple (MAE en temps réel, carte des zones chaudes),
**afin de** suivre la performance de mes livreurs sans ouvrir de code.

**Estimation :** 8 points — **Reporté Sprint 2**

---

### US-10 ★☆☆ COULD
**En tant que** Data Scientist,
**je veux** un modèle de prédiction géographique (clustering des zones de forte demande),
**afin de** pré-positionner les coursiers par quartier aux heures de pointe.

**Estimation :** 13 points — **Reporté Sprint 2**

---

## Récapitulatif Sprint 1

| ID    | Priorité | Points | Statut      |
|-------|----------|--------|-------------|
| US-01 | MUST     | 3      | ✅ Terminé  |
| US-02 | MUST     | 2      | ✅ Terminé  |
| US-03 | MUST     | 2      | ✅ Terminé  |
| US-04 | MUST     | 5      | ✅ Terminé  |
| US-05 | SHOULD   | 3      | ✅ Terminé  |
| US-06 | SHOULD   | 2      | ✅ Terminé  |
| US-07 | MUST     | 1      | ✅ Terminé  |
| US-08 | SHOULD   | 1      | ✅ Terminé  |

**Vélocité Sprint 1 : 19 points**
