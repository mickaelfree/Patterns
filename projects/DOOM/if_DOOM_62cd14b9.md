---
tags: pattern, pattern/if, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: if
pattern_variant: simple
source_file: p_map.c
line: 1298
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `p_map.c`
- **Ligne**: 1298
- **Fonction**: PIT_ChangeSector
- **Projet**: DOOM
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (crushchange && !(leveltime&3) )
    {
	P_DamageMobj(thing,NULL,NULL,10);

	// spray blood in a random direction
	mo = P_SpawnMobj (thing->x,
			  thing->y,
			  thing->z + thing->height/2, MT_BLOOD);
	
	mo->momx = (P_Random() - P_Random ())<<12;
	mo->momy = (P_Random() - P_Random ())<<12;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_DOOM_1a1f040c|p_spec.c:1040]] (P_PlayerInSpecialSector)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[else_DOOM_15ea13cc|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_0faf1aab|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_29abfc46|🔀 Répartiteur alternatif (ELSE)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
[[switch_DOOM_83fe174e|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_17419957|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_b47d2988|🔀 Aiguillage multiple (SWITCH)]]
