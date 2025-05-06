---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: init_mutex.c
line: 30
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 30
- **Fonction**: free_all_fork
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (data->all_fork)
	{
		while (data->all_fork[++i])
		{
			pthread_mutex_destroy(data->all_fork[i]);
			free(data->all_fork[i]);
		}
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_b4d9dacc|init_mutex.c:30]] (free_all_fork)
- [[if_philo_b4d9dacc|init_mutex.c:30]] (free_all_fork)
- [[if_philo_b4d9dacc|init_mutex.c:30]] (free_all_fork)
- [[if_philo_b4d9dacc|init_mutex.c:30]] (free_all_fork)
- [[if_philo_b4d9dacc|init_mutex.c:30]] (free_all_fork)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[else_if_philo_b93d7788|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_d9b36d2b|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_106ac6f7|🔄 Répartiteur intelligent (ELSE IF)]]
