---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: take_fork.c
line: 39
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `take_fork.c`
- **Ligne**: 39
- **Fonction**: give_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	ft_take_fork(t_philo *philo, t_data *d, t_parametre p, t_all_mutex m)
{
	if (!is_finish(d, m))
		return (1);
	ft_message(d, philo, "has taken a fork", m);
	pthread_mutex_lock(m.all_fork[philo->first_fork]);
	if (p.n_philo != 1)
	{
		pthread_mutex_lock(m.all_fork[philo->second_fork]);
		ft_message(d, philo, "has taken a fork", m);
	}
	else
		ft_sleep(d, m, p.t_die);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_9d4a2e9f|take_fork.c:51]] (give_fork)
- [[function_philo_40238030|routine_and_fork.c:26]] (give_fork)
- [[function_philo_40238030|routine_and_fork.c:26]] (give_fork)
- [[function_philo_64b31b31|take_fork.c:74]] (get_first_fork)
- [[function_philo_df95f54b|sleep.c:15]] (philo_sleep)

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
