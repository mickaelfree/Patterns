---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: simulation_bonus.c
line: 23
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `simulation_bonus.c`
- **Ligne**: 23
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (get_current_time() - philo->times.last_meal > philo->times.die)
		{
			print_action(philo, RED"died"RESET);
			sem_wait(philo->sems->write_sem);
			sem_post(philo->sems->meal_sem);
			exit(EXIT_SUCCESS);
		}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_0a41fb7f|grim_reaper.c:105]] (end_condition_reached)
- [[if_philo_d9e68386|grim_reaper.c:58]] (kill_philo)

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
