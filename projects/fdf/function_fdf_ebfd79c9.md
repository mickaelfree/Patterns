---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: get_next_line.c
line: 31
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `get_next_line.c`
- **Ligne**: 31
- **Fonction**: ft_find_newline
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static ssize_t	ft_find_newline(char *str)
{
	char	*start;

	start = str;
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
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_fdf_2a890ee3|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_3fed850e|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_b83d5c36|🚚 Convoyeur de sortie (RETURN)]]
