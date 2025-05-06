---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: gestion_thread.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `gestion_thread.c`
- **Ligne**: 15
- **Fonction**: someone_died
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static int	someone_died(t_philo *philo, t_data *data, long duration)
{
	pthread_mutex_lock(data->mutexs.eat);
	if (data->param.n_eat != -1 && data->param.n_eat <= philo->nbr_eat)
		return (pthread_mutex_unlock(data->mutexs.eat), 0);
	if (duration - philo->t_last_eat >= (long)data->param.t_die)
	{
		pthread_mutex_unlock(data->mutexs.eat);
		pthread_mutex_lock(data->mutexs.check);
		data->evryone_is_alive = FALSE;
		pthread_mutex_lock(data->mutexs.use_printf);
		data->one_dead = TRUE;
		printf("%ld %d died\n", duration, philo->id + 1);
		pthread_mutex_unlock(data->mutexs.use_printf);
		pthread_mutex_unlock(data->mutexs.check);
		return (1);
	}
	pthread_mutex_unlock(data->mutexs.eat);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
