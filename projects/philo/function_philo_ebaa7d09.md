---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: take_fork.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `take_fork.c`
- **Ligne**: 15
- **Fonction**: give_first_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	give_first_fork(t_philo *philo, t_parametre p, t_all_mutex m)
{
	int	index_fork;

	if (philo->id % 2 == 0)
		index_fork = philo->id;
	else
		index_fork = philo->id + 1;
	if (index_fork == p.n_philo)
		index_fork = 0;
	pthread_mutex_unlock(m.all_fork[index_fork]);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_56eb0823|take_fork.c:61]] (get_second_fork)
- [[function_philo_89cca348|take_fork.c:48]] (give_fork)
- [[function_philo_9ead4534|init_philo.c:28]] (get_second_fork)
- [[function_philo_9ead4534|init_philo.c:28]] (get_second_fork)
- [[function_philo_545ba396|init_free_philo.c:28]] (get_second_fork)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 3 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
