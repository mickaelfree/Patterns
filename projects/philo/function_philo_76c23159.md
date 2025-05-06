---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: parsing.c
line: 41
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `parsing.c`
- **Ligne**: 41
- **Fonction**: parsing
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	parsing(int argc, char **argv, int get_arg, int *error)
{
	int	res;

	if (*error)
		return (0);
	res = 0;
	get_arg = get_arg + 1;
	if (argc < 5 || argc > 6)
		return (*error = 2, printf("\nERROR: NOMBRE d'argument non valide\n"), 0);
	if (get_arg == 5 && argc == 5)
		return (-1);
	res = ft_atoi(argv[get_arg], error);
	if (*error == 0 && res == 0 && get_arg == 1)
		*error = 3;
	if (*error == 2)
		printf("\nERROR: Argument %d NULL ou ne contient rien.\n", get_arg);
	else if (*error == 3)
		printf("\nERROR: Argument %d NON valide.\n\
Caractere non valide | OU | VALEUR interdite.\n\n", get_arg);
	if (*error)
		*error = 2;
	return (res);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_826d933c|parsing.c:41]] (parsing)
- [[function_philo_49ec1c29|parsing.c:40]] (parsing)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
