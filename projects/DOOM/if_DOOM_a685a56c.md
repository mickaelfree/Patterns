---
tags: pattern, pattern/if, factorio, code-logic, project/DOOM, pattern/variant/nested
date: 2025-04-25
pattern_type: if
pattern_variant: nested
source_file: p_map.c
line: 214
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `p_map.c`
- **Ligne**: 214
- **Fonction**: PIT_CheckLine
- **Projet**: DOOM
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (!(tmthing->flags & MF_MISSILE) )
    {
	if ( ld->flags & ML_BLOCKING )
	    return false;	// explicitly blocking everything

	if ( !tmthing->player && ld->flags & ML_BLOCKMONSTERS )
	    return false;	// block monsters only
    }
```

## Analyse Structurelle
**Type détecté**: Capteur en cascade

Ces capteurs en cascade pourraient être combinés en un seul réseau logique avec des opérateurs && ou ||.

**Analogie Factorio**:
Comme plusieurs capteurs en série dans Factorio que vous pourriez remplacer par un circuit combinatoire unique.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_DOOM_41b75c18|p_map.c:825]] (PTR_AimTraverse)
- [[if_DOOM_91ffbf6f|p_map.c:466]] (global)
- [[if_DOOM_2c2afaa0|p_map.c:291]] (if)
- [[if_DOOM_80c085c8|p_map.c:331]] (if)
- [[if_DOOM_37812d50|p_map.c:1290]] (PIT_ChangeSector)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

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
