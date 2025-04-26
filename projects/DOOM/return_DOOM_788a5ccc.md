---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: r_main.c
line: 184
project: DOOM
first_seen: 2025-04-25
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `r_main.c`
- **Ligne**: 184
- **Fonction**: R_PointOnSide
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return node->dx > 0;
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_8aa4c41d|p_sight.c:71]] (P_DivlineSide)
- [[return_DOOM_5921bf95|p_sight.c:82]] (P_DivlineSide)
- [[return_DOOM_8aa4c41d|p_sight.c:71]] (P_DivlineSide)
- [[return_DOOM_5921bf95|p_sight.c:82]] (P_DivlineSide)
- [[return_DOOM_92c37bd9|p_maputl.c:88]] (P_PointOnLineSide)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_DOOM_d7c161a6|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_17b7a3b4|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_cabafe97|🏭 Usine modulaire (FUNCTION)]]
