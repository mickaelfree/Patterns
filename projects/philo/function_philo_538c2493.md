---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_mutex.c
line: 42
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 42
- **Fonction**: free_all_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
t_all_mutex	init_mutex(int *err, int nombre_de_philo)
{
	t_all_mutex	mutexs;

	if (*err)
	{
		mutexs.all_fork = NULL;
		mutexs.check = NULL;
		return (mutexs.eat = NULL, mutexs.use_printf = NULL, mutexs);
	}
	mutexs.use_printf = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!mutexs.use_printf)
		*(err) = 1;
	else if (pthread_mutex_init(mutexs.use_printf, NULL))
		*(err) = 6;
	mutexs.check = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!mutexs.check)
		*(err) = 1;
	else if (pthread_mutex_init(mutexs.check, NULL))
		*(err) = 6;
	mutexs.eat = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!mutexs.eat)
		*(err) = 1;
	else if (pthread_mutex_init(mutexs.eat, NULL))
		*(err) = 6;
	init_all_fork(&mutexs, -1, nombre_de_philo, err);
	return (mutexs);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
