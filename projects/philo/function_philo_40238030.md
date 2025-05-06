---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: routine_and_fork.c
line: 26
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `routine_and_fork.c`
- **Ligne**: 26
- **Fonction**: give_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	ft_take_fork(t_philo *philo, t_data *data)
{
	if (!is_finish(data))
		return (1);
	ft_message(philo, "has taken a fork", data->mutexs);
	pthread_mutex_lock(data->mutexs.all_fork[philo->first_fork]);
	if (data->param.n_philo != 1)
	{
		pthread_mutex_lock(data->mutexs.all_fork[philo->second_fork]);
		ft_message(philo, "has taken a fork", data->mutexs);
	}
	else
		ft_sleep(data->param.t_die);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_9d4a2e9f|take_fork.c:51]] (give_fork)
- [[function_philo_272008d6|eat_sleep_think.c:36]] (philo_sleep)
- [[function_philo_f487c63f|eat_sleep_think.c:36]] (philo_sleep)

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
