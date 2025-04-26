---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: w_wad.c
line: 408
project: DOOM
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `w_wad.c`
- **Ligne**: 408
- **Fonction**: W_GetNumForName
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return i;
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_01d473b3|i_sound.c:489]] (I_StartSound)
- [[return_DOOM_01d473b3|i_sound.c:489]] (I_StartSound)
- [[return_DOOM_498ada47|p_spec.c:374]] (P_FindNextHighestFloor)
- [[return_DOOM_498ada47|p_spec.c:374]] (P_FindNextHighestFloor)
- [[return_DOOM_650ccd10|d_net.c:107]] (NetbufferChecksum)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_DOOM_d7c161a6|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_17b7a3b4|🏭 Usine modulaire (FUNCTION)]]
[[function_DOOM_cabafe97|🏭 Usine modulaire (FUNCTION)]]
