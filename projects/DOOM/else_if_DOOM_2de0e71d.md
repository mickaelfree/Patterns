---
tags: pattern, pattern/else-if, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else if
pattern_variant: simple
source_file: p_user.c
line: 371
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Répartiteur intelligent (ELSE IF) (Filtrage simple)

## Contexte
- **Fichier**: `p_user.c`
- **Ligne**: 371
- **Fonction**: if
- **Projet**: DOOM
- **Variante**: Filtrage simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Répartiteur intelligent**

Comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.

## Code Source
```c
else if (player->powers[pw_infrared])	
    {
	if (player->powers[pw_infrared] > 4*32
	    || (player->powers[pw_infrared]&8) )
	{
	    // almost full bright
	    player->fixedcolormap = 1;
	}
	else
	    player->fixedcolormap = 0;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur intelligent dans Factorio. Il comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.*

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
[[else_DOOM_15ea13cc|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_0faf1aab|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_29abfc46|🔀 Répartiteur alternatif (ELSE)]]
[[switch_DOOM_83fe174e|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_17419957|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_b47d2988|🔀 Aiguillage multiple (SWITCH)]]
