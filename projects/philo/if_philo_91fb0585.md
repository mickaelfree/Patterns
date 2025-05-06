---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: check.c
line: 25
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 25
- **Fonction**: la_morgue
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (duration - philo->t_last_eat - (now - duration) >= (long)p.t_die)
	{
		pthread_mutex_unlock(m.eat);
		// duration = get_time_pass(d->t_start, &(d->err));
		pthread_mutex_lock(m.check);
		d->evryone_is_alive = FALSE;
		pthread_mutex_lock(m.use_printf);
		d->time_of_death = duration;
		printf("%ld - %ld - (%ld - %ld) >= %d\n", duration, philo->t_last_eat, now, duration, p.t_die);
		printf("%ld %d \tdied\n", duration, philo->id);
		pthread_mutex_unlock(m.use_printf);
		return (pthread_mutex_unlock(m.check), 1);
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

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
