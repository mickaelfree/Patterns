---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: thread.c
line: 31
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `thread.c`
- **Ligne**: 31
- **Fonction**: is_finish
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	ft_take_fork(t_philo *philo)
{
	t_data	*d;
	int		index_fork;

	d = philo->data;
	if (philo->id % 2 == 0)
		index_fork = philo->id;
	else
		index_fork = philo->id + 1;
	if (index_fork == philo->data->n_philo)
		index_fork = 0;
	pthread_mutex_lock(d->all_fork[index_fork]);
	ft_message(get_time_pass(d->t_start, &(d->err)), philo->id, "has taken a fork 1", d);
	if (d->n_philo != 1)
	{
		if (philo->id % 2 == 0)
			index_fork = philo->id + 1;
		else
			index_fork = philo->id;
		if (index_fork == philo->data->n_philo)
			index_fork = 0;
		pthread_mutex_lock(d->all_fork[index_fork]);
		ft_message(get_time_pass(d->t_start, &(d->err)), philo->id, "has taken a fork 2", d);
	}
	else
		ft_sleep(d, d->t_die);
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
