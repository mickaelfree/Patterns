---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: thread.c
line: 60
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `thread.c`
- **Ligne**: 60
- **Fonction**: ft_take_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	ft_eat(t_philo *philo, t_data *d)
{
	ft_message(get_time_pass(d->t_start, &(d->err)), philo->id, "is eating", d);
	philo->nbr_eat++;

	pthread_mutex_lock(d->eat);
	if (philo->nbr_eat == d->n_eat)
		d->evryone_eat++;
	pthread_mutex_unlock(d->eat);
	
	philo->t_last_eat = get_time_pass(d->t_start, &(d->err));
	ft_sleep(d, d->t_eat);
	
	pthread_mutex_unlock(d->all_fork[philo->id]);
	if (d->n_philo != 1 && d->n_philo - 1 != philo->id)
		pthread_mutex_unlock(d->all_fork[philo->id + 1]);
	else if (d->n_philo - 1 == philo->id)
		pthread_mutex_unlock(d->all_fork[0]);
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
