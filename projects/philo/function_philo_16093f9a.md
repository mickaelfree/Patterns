---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: check.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 15
- **Fonction**: la_morgue
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	la_morgue(t_philo *philo, t_parametre p, t_all_mutex m, long duration)
{
	t_data	*d;

	d = philo->data;
	pthread_mutex_lock(m.eat);
	if (p.n_eat != -1 && p.n_eat <= philo->nbr_eat)
		return (pthread_mutex_unlock(m.eat), 0);
	if (duration - philo->t_last_eat >= p.t_die)
	{
		pthread_mutex_unlock(m.eat);
		duration = get_time_pass(d->t_start, &(d->err));
		pthread_mutex_lock(m.check);
		d->evryone_is_alive = FALSE;
		pthread_mutex_lock(m.use_printf);
		d->time_of_death = duration;
		printf("%ld %d \tdied\n", duration, philo->id);
		pthread_mutex_unlock(m.use_printf);
		return (pthread_mutex_unlock(m.check), 1);
	}
	return (pthread_mutex_unlock(m.eat), 0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_45b800cc|check.c:15]] (la_morgue)
- [[function_philo_f40035a6|check.c:15]] (la_morgue)

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
