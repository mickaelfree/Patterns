---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: init_free_all_mutex.c
line: 41
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `init_free_all_mutex.c`
- **Ligne**: 41
- **Fonction**: free_all_fork
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (mutexs.all_fork)
	{
		while (mutexs.all_fork[++i])
		{
			pthread_mutex_destroy(mutexs.all_fork[i]);
			free(mutexs.all_fork[i]);
		}
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_f474db8e|init_mutex.c:30]] (free_all_fork)
- [[if_philo_070b610c|routine_and_fork.c:17]] (give_fork)
- [[if_philo_070b610c|routine_and_fork.c:17]] (give_fork)
- [[if_philo_4048a94c|take_fork.c:30]] (give_fork)
- [[if_philo_971d555d|take_fork.c:32]] (give_fork)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 5 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[else_if_philo_b93d7788|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_d9b36d2b|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_106ac6f7|🔄 Répartiteur intelligent (ELSE IF)]]
