---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: p_maputl.c
line: 181
project: DOOM
first_seen: 2025-04-25
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `p_maputl.c`
- **Ligne**: 181
- **Fonction**: P_PointOnDivlineSide
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return line->dx < 0;
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_7c6c3b3a|p_maputl.c:81]] (P_PointOnLineSide)
- [[return_DOOM_92c37bd9|p_maputl.c:88]] (P_PointOnLineSide)
- [[return_DOOM_7c6c3b3a|p_maputl.c:81]] (P_PointOnLineSide)
- [[return_DOOM_92c37bd9|p_maputl.c:88]] (P_PointOnLineSide)
- [[return_DOOM_7bcb9552|p_maputl.c:79]] (P_PointOnLineSide)

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
