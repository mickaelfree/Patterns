---
tags: pattern, pattern/else, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else
pattern_variant: simple
source_file: p_inter.c
line: 539
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Répartiteur alternatif (ELSE) (Répartiteur simple)

## Contexte
- **Fichier**: `p_inter.c`
- **Ligne**: 539
- **Fonction**: P_TouchSpecialThing
- **Projet**: DOOM
- **Variante**: Répartiteur simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Répartiteur alternatif**

Comme un répartiteur qui dirige les ressources vers un chemin alternatif.

## Code Source
```c
else
	{
	    if (!P_GiveAmmo (player,am_clip,1))
		return;
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur alternatif dans Factorio. Il comme un répartiteur qui dirige les ressources vers un chemin alternatif.*

## Patterns Similaires
- [[else_DOOM_7d3a4703|p_doors.c:428]] (global)
- [[else_DOOM_0bae187b|p_pspr.c:357]] (A_ReFire)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
