---
tags: pattern, pattern/else-if, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else if
pattern_variant: simple
source_file: f_wipe.c
line: 196
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Répartiteur intelligent (ELSE IF) (Filtrage simple)

## Contexte
- **Fichier**: `f_wipe.c`
- **Ligne**: 196
- **Fonction**: if
- **Projet**: DOOM
- **Variante**: Filtrage simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Répartiteur intelligent**

Comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.

## Code Source
```c
else if (y[i] < height)
	    {
		dy = (y[i] < 16) ? y[i]+1 : 8;
		if (y[i]+dy >= height) dy = height - y[i];
		s = &((short *)wipe_scr_end)[i*height+y[i]];
		d = &((short *)wipe_scr)[y[i]*width+i];
		idx = 0;
		for (j=dy;j;j--)
		{
		    d[idx] = *(s++);
		    idx += width;
		}
		y[i] += dy;
		s = &((short *)wipe_scr_start)[i*height];
		d = &((short *)wipe_scr)[y[i]*width+i];
		idx = 0;
		for (j=height-y[i];j;j--)
		{
		    d[idx] = *(s++);
		    idx += width;
		}
		done = false;
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
