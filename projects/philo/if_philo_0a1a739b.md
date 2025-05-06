---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: if
pattern_variant: simple
source_file: check.c
line: 23
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 23
- **Fonction**: la_morgue
- **Projet**: philo
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (duration - philo->t_last_eat >= (long)p.t_die)
	{
		pthread_mutex_unlock(m.eat);
		pthread_mutex_lock(m.check);
		d->evryone_is_alive = FALSE;
		pthread_mutex_lock(m.use_printf);
		d->one_dead = TRUE;
		printf("%ld %d died\n", duration, philo->id + 1);
		pthread_mutex_unlock(m.use_printf);
		return (pthread_mutex_unlock(m.check), 1);
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_philo_b0ce4c28|gestion_thread.c:20]] (someone_died)
- [[if_philo_b0ce4c28|gestion_thread.c:20]] (someone_died)
- [[if_philo_2afff2f7|check.c:23]] (la_morgue)

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
