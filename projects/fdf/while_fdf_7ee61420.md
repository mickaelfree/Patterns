---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: fdf.c
line: 178
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 178
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (i < map->height)
	{
		map->points[i] = (t_point *)malloc(sizeof(t_point) * map->width);
		if (!map->points[i])
		{
			while (--i >= 0)
				free(map->points[i]);
			free(map->points);
			free(map);
			close(fd);
			return (NULL);
		}
		line = get_next_line(fd);
		if (!line)
			break;
		split = ft_split(line, ' ');
		j = 0;
		while (j < map->width && split[j])
		{
			map->points[i][j].x = j;
			map->points[i][j].y = i;
			map->points[i][j].z = ft_atoi(split[j]);
			map->points[i][j].color = parse_color(split[j]);
			j++;
		}
		free_split(split);
		free(line);
		i++;
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
