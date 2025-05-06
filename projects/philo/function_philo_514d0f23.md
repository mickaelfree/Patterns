---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: check.c
line: 37
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 37
- **Fonction**: la_morgue
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	evryone_eat(t_data *d, t_parametre p, t_all_mutex m)
{
	int		i;
	t_philo	*philo;

	i = 0;
	while (d->all_philo[i])
	{
		philo = d->all_philo[i++];
		pthread_mutex_lock(m.eat);
		if (p.n_eat == -1 || p.n_eat > philo->nbr_eat)
			return (pthread_mutex_unlock(m.eat), 0);
		pthread_mutex_unlock(m.eat);
	}
	pthread_mutex_lock(m.check);
	d->evryone_is_alive = FALSE;
	pthread_mutex_unlock(m.check);
	return (1);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_8f90b5e2|check.c:38]] (la_morgue)
- [[function_philo_e622384e|gestion_thread.c:36]] (someone_died)
- [[function_philo_e622384e|gestion_thread.c:36]] (someone_died)

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
