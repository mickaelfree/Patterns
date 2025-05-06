---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: parsing.c
line: 48
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `parsing.c`
- **Ligne**: 48
- **Fonction**: parsing
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_parsing(t_data *data, int argc, char **argv)
{
	if (argc < 5 || argc > 6)
		data->err = 2;
	data->n_philo = parsing(argc, argv, 0, &(data->err));
	data->t_die = parsing(argc, argv, 1, &(data->err));
	data->t_eat = parsing(argc, argv, 2, &(data->err));
	data->t_sleep = parsing(argc, argv, 3, &(data->err));
	data->n_eat = parsing(argc, argv, 4, &(data->err));
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_4be16d8a|parsing.c:48]] (parsing)
- [[function_philo_85cbc232|init_parsing.c:52]] (parsing)

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
