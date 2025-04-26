---
tags: pattern, pattern/return, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: wadread.c
line: 118
project: DOOM
first_seen: 2025-04-25
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `wadread.c`
- **Ligne**: 118
- **Fonction**: SwapSHORT
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return
	(x>>8) | (x<<8);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_DOOM_571e7a36|p_maputl.c:56]] (P_AproxDistance)
- [[return_DOOM_e5285c53|s_sound.c:817]] (S_AdjustSoundParams)
- [[return_DOOM_9ac98090|r_main.c:245]] (R_PointOnSegSide)
- [[return_DOOM_b945d8f8|r_main.c:247]] (R_PointOnSegSide)
- [[return_DOOM_90acaa54|m_fixed.c:77]] (FixedDiv2)

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
