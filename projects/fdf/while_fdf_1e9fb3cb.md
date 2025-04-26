---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/potential_infinite
date: 2025-04-25
pattern_type: while
pattern_variant: potential_infinite
source_file: fdf.c
line: 297
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 297
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (i < data->map->height)
	{
		j = 0;
		while (j < data->map->width)
		{
			p1 = project_point(data->map->points[i][j], data);
			
			if (j + 1 < data->map->width)
			{
				p2 = project_point(data->map->points[i][j + 1], data);
				draw_line(data, p1, p2);
			}
			
			if (i + 1 < data->map->height)
			{
				p2 = project_point(data->map->points[i + 1][j], data);
				draw_line(data, p1, p2);
			}
			j++;
		}
		i++;
	}
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[for_fdf_aa045c10|🔄 Chaîne de montage (FOR)]]
[[for_fdf_b3efebf6|🔄 Chaîne de montage (FOR)]]
[[for_fdf_c97cbea4|🔄 Chaîne de montage (FOR)]]
