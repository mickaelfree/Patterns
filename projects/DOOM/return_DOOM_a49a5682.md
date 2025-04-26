---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: p_floor.c
line: 180
project: DOOM
first_seen: 2025-04-25
occurrences: 4
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `p_floor.c`
- **Ligne**: 180
- **Fonction**: switch
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return pastdest;
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_97e34f47|r_main.c:417]] (R_PointToDist)
- [[return_DOOM_e198b61b|am_map.c:888]] (AM_clipMline)
- [[return_DOOM_e198b61b|am_map.c:888]] (AM_clipMline)
- [[return_DOOM_e198b61b|am_map.c:888]] (AM_clipMline)
- [[return_DOOM_e198b61b|am_map.c:888]] (AM_clipMline)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 4 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_DOOM_d7c161a6|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_17b7a3b4|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_cabafe97|🏭 Usine modulaire (FUNCTION)]]
