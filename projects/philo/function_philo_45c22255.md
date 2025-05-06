---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_bonus.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_bonus.c`
- **Ligne**: 15
- **Fonction**: init_philos
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_philos(t_engine *engine, char **argv, int count)
{
	t_philo	**philos;
	int		i;

	i = -1;
	philos = engine->philos;
	while (++i < count)
	{
		philos[i] = (t_philo *)malloc(sizeof(t_philo));
		if (!philos[i])
			destroy_all(engine, "[Malloc ERROR]\n", true, EXIT_FAILURE);
		philos[i]->id = i + 1;
		philos[i]->sems = engine->sems;
		philos[i]->times.die = ft_atoi(argv[2]);
		philos[i]->times.eat = ft_atoi(argv[3]);
		philos[i]->times.sleep = ft_atoi(argv[4]);
		philos[i]->times.last_meal = get_current_time();
		philos[i]->times.born_time = get_current_time();
		philos[i]->must_eat = -1;
		if (argv[5])
			philos[i]->must_eat = ft_atoi(argv[5]);
		philos[i]->meals_eaten = 0;
		philos[i]->philo_count = count;
	}
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
