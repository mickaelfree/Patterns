---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: r_bsp.c
line: 486
project: DOOM
first_seen: 2025-04-25
occurrences: 130
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `r_bsp.c`
- **Ligne**: 486
- **Fonction**: R_CheckBBox
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return true;
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_4ac3e7a3|p_map.c:1110]] (PTR_UseTraverse)
- [[return_DOOM_b6ab7745|i_sound.c:975]] (I_SoundSetTimer)
- [[return_DOOM_35ab95f2|z_zone.c:465]] (Z_FreeMemory)
- [[return_DOOM_3e1b4f0f|am_map.c:733]] (if)
- [[return_DOOM_3e1b4f0f|am_map.c:733]] (if)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 130 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_DOOM_d7c161a6|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_17b7a3b4|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_cabafe97|🏭 Usine modulaire (FUNCTION)]]
