---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: take_fork.c
line: 45
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `take_fork.c`
- **Ligne**: 45
- **Fonction**: ft_take_fork
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (p.n_philo != 1)
	{
		pthread_mutex_lock(m.all_fork[philo->second_fork]);
		ft_message(d, philo, "has taken a fork", m);
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_8820aefb|routine_and_fork.c:32]] (ft_take_fork)
- [[if_philo_8820aefb|routine_and_fork.c:32]] (ft_take_fork)
- [[if_philo_b0d3c659|take_fork.c:57]] (ft_take_fork)
- [[if_philo_4048a94c|take_fork.c:30]] (give_fork)
- [[if_philo_070b610c|routine_and_fork.c:17]] (give_fork)

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
