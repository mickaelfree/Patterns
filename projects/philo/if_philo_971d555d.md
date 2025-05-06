---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/nested
date: 2025-05-07
pattern_type: if
pattern_variant: nested
source_file: take_fork.c
line: 32
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `take_fork.c`
- **Ligne**: 32
- **Fonction**: give_fork
- **Projet**: philo
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (p.n_philo > 1)
	{
		pthread_mutex_unlock(m.all_fork[philo->first_fork]);
		pthread_mutex_unlock(m.all_fork[philo->second_fork]);

		// if (philo->id % 2 == 0)
		// 	index_fork = philo->id + 1;
		// else
		// 	index_fork = philo->id;
		// if (index_fork == p.n_philo)
		// 	index_fork = 0;
		// pthread_mutex_unlock(m.all_fork[index_fork]);
		// give_first_fork(philo, p, m);
	}
```

## Analyse Structurelle
**Type détecté**: Capteur en cascade

Ces capteurs en cascade pourraient être combinés en un seul réseau logique avec des opérateurs && ou ||.

**Analogie Factorio**:
Comme plusieurs capteurs en série dans Factorio que vous pourriez remplacer par un circuit combinatoire unique.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_4048a94c|take_fork.c:30]] (give_fork)
- [[if_philo_4b75acf8|take_fork.c:45]] (ft_take_fork)
- [[if_philo_8820aefb|routine_and_fork.c:32]] (ft_take_fork)
- [[if_philo_8820aefb|routine_and_fork.c:32]] (ft_take_fork)
- [[if_philo_8b90873d|philosopher.c:32]] (eat_sleep_routine)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_if_philo_b93d7788|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_d9b36d2b|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_philo_106ac6f7|🔄 Répartiteur intelligent (ELSE IF)]]
