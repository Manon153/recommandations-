# Definition of Done (DoD) — Green & Fast 2026

> Une tâche est considérée comme **TERMINÉE** si et seulement si tous les critères
> ci-dessous sont cochés.

---

## Critères généraux (toutes tâches)

- [ ] **Code relu** par au moins un autre membre de l'équipe (peer review)
- [ ] **Tests passés** : le script s'exécute sans erreur de bout en bout
- [ ] **Push sur la branche `main`** (ou branche feature mergée via PR)
- [ ] **Commit message clair** : décrit ce qui a été fait (`feat:`, `fix:`, `data:`, `docs:`)
- [ ] **Pas de credentials** ou données sensibles dans le dépôt

---

## Critères spécifiques — Tâches Data

- [ ] Aucune valeur manquante dans les colonnes utilisées par le modèle
- [ ] Les types de données sont corrects (int, float, str) après nettoyage
- [ ] La distribution de la variable cible est vérifiée (pas de valeurs aberrantes extrêmes)
- [ ] Le code de nettoyage est commenté et explique le "pourquoi" de chaque transformation

---

## Critères spécifiques — Tâches Modèle

- [ ] Les métriques MAE et RMSE sont affichées et documentées
- [ ] Le split train/test est fixé (`random_state=42`) pour reproductibilité
- [ ] Les résultats sont comparables entre les membres de l'équipe (même seed)
- [ ] La performance est jugée acceptable par l'équipe **avant** de merger

---

## Critères spécifiques — Documentation

- [ ] README mis à jour si le comportement du script change
- [ ] Les nouvelles features ajoutées au tableau de features du README
- [ ] Le Kanban est mis à jour (tâche déplacée en colonne "Terminé")
- [ ] Le Backlog est mis à jour (statut de la User Story)

---

## Critères de qualité minimale (Sprint 1)

| Métrique | Seuil acceptable |
|----------|-----------------|
| MAE      | < 8 minutes      |
| RMSE     | < 10 minutes     |
| Couverture nettoyage | 100% des colonnes traitées |

---

*Validé par l'équipe le 20/03/2026*
