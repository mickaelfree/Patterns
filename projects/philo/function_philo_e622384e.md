---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: gestion_thread.c
line: 36
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `gestion_thread.c`
- **Ligne**: 36
- **Fonction**: someone_died
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static int	evryone_to_eat(t_data *data)
{
	int		i;
	t_philo	*philo;

	i = -1;
	while (data->all_philo[++i])
	{
		philo = data->all_philo[i];
		pthread_mutex_lock(data->mutexs.eat);
		if (data->param.n_eat == -1 || data->param.n_eat > philo->nbr_eat)
			return (pthread_mutex_unlock(data->mutexs.eat), 0);
		pthread_mutex_unlock(data->mutexs.eat);
	}
	pthread_mutex_lock(data->mutexs.check);
	data->evryone_is_alive = FALSE;
	pthread_mutex_unlock(data->mutexs.check);
	return (1);
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
