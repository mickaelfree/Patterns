---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_parsing.c
line: 35
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_parsing.c`
- **Ligne**: 35
- **Fonction**: ft_atoi
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static int	parsing(int argc, char **argv, int get_arg, int *error)
{
	int	res;

	get_arg++;
	if (*error || (get_arg == 5 && argc == 5))
		return (-1);
	res = ft_atoi(argv[get_arg], error);
	if (*error)
		return (res);
	else if (get_arg >= 1 && get_arg <= 2 && !res)
		*error = 4;
	else if (get_arg >= 1 && res > 1000)
		*error = 4;
	return (res);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_f217761a|parsing.c:35]] (ft_atoi)
- [[function_philo_f217761a|parsing.c:35]] (ft_atoi)
- [[function_philo_f217761a|parsing.c:35]] (ft_atoi)
- [[function_philo_f217761a|parsing.c:35]] (ft_atoi)
- [[function_philo_f217761a|parsing.c:35]] (ft_atoi)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
