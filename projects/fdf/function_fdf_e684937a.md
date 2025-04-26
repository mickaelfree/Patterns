---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: get_next_line.c
line: 108
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `get_next_line.c`
- **Ligne**: 108
- **Fonction**: main
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	main(void)
{
	int		file_descriptor;
	char	*line;

	file_descriptor = open("big_line_no_nl", O_RDONLY);
	if (file_descriptor == -1)
		return (1);
	while ((line = get_next_line(file_descriptor)))
	{
		printf("%s\n", line);
		free(line);
	}
	close(file_descriptor);
	return (0);
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
