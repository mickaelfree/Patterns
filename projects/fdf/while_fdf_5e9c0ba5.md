---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: get_next_line.c
line: 36
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `get_next_line.c`
- **Ligne**: 36
- **Fonction**: ft_find_newline
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
		if (!str[0])
			return (-1);
		if (str[0] == '\n')
			return (str - start);
		if (!str[1])
			return (-1);
		if (str[1] == '\n')
			return (str - start + 1);
		if (!str[2])
			return (-1);
		if (str[2] == '\n')
			return (str - start + 2);
		if (!str[3])
			return (-1);
		if (str[3] == '\n')
			return (str - start + 3);
		str += 4;
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_fdf_4be7f7d8|get_next_line_utils.c:48]] (ft_strlen)

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
