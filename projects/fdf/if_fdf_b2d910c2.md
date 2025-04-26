---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: if
pattern_variant: simple
source_file: fdf.c
line: 159
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 159
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (map->height == 0 || map->width == 0)
	{
		free(map);
		return (NULL);
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_fdf_beb586e6|fdf.c:165]] (global)
- [[if_fdf_ae7ab6ed|fdf.c:171]] (global)
- [[if_fdf_4e629eb6|split.c:85]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[else_fdf_1041c8ff|🔀 Répartiteur alternatif (ELSE)]]
[[else_fdf_16c235a8|🔀 Répartiteur alternatif (ELSE)]]
