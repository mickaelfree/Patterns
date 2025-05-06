---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_parsing.c
line: 52
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_parsing.c`
- **Ligne**: 52
- **Fonction**: parsing
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
t_parametre	init_parsing(int *err, int argc, char **argv)
{
	t_parametre	param;

	if (argc < 5 || argc > 6)
		*(err) = 2;
	param.n_philo = parsing(argc, argv, 0, err);
	param.t_die = parsing(argc, argv, 1, err);
	param.t_eat = parsing(argc, argv, 2, err);
	param.t_sleep = parsing(argc, argv, 3, err);
	param.n_eat = parsing(argc, argv, 4, err);
	if (param.n_philo % 2)
		param.is_impaire = TRUE;
	else
		param.is_impaire = FALSE;
	return (param);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_6c5142d2|parsing.c:48]] (parsing)

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
