---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: fdf.c
line: 239
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 239
- **Fonction**: draw_line
- **Projet**: fdf
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (1)
	{
		my_mlx_pixel_put(data, p1.x, p1.y, color);
		if (p1.x == p2.x && p1.y == p2.y)
			break;
		e2 = 2 * err;
		if (e2 > -dy)
		{
			err -= dy;
			p1.x += sx;
		}
		if (e2 < dx)
		{
			err += dx;
			p1.y += sy;
		}
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[for_fdf_aa045c10|🔄 Chaîne de montage (FOR)]]
[[for_fdf_b3efebf6|🔄 Chaîne de montage (FOR)]]
[[for_fdf_c97cbea4|🔄 Chaîne de montage (FOR)]]
