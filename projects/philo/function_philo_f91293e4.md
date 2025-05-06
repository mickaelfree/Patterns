---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_mutex.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 15
- **Fonction**: init_all_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_all_fork(t_all_mutex *mutexs, int i, int nombre_de_philo, int *err)
{
	mutexs->all_fork = ft_calloc(nombre_de_philo, sizeof(pthread_mutex_t));
	if (!mutexs->all_fork)
		*err = 1;
	while (!(*err) && ++i < nombre_de_philo)
	{
		mutexs->all_fork[i] = ft_calloc(1, sizeof(pthread_mutex_t));
		if (pthread_mutex_init(mutexs->all_fork[i], NULL))
			*err = 6;
	}
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_64f64532|init_free_all_mutex.c:15]] (init_all_fork)
- [[function_philo_64f64532|init_free_all_mutex.c:15]] (init_all_fork)
- [[function_philo_10ee275b|init_mutex.c:15]] (init_all_fork)

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
