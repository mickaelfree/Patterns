---
tags: pattern, pattern/if, factorio, code-logic, project/philo, pattern/variant/nested
date: 2025-05-07
pattern_type: if
pattern_variant: nested
source_file: thread.c
line: 45
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `thread.c`
- **Ligne**: 45
- **Fonction**: ft_take_fork
- **Projet**: philo
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (d->n_philo != 1)
	{
		if (philo->id % 2 == 0)
			index_fork = philo->id + 1;
		else
			index_fork = philo->id;
		if (index_fork == philo->data->n_philo)
			index_fork = 0;
		pthread_mutex_lock(d->all_fork[index_fork]);
		ft_message(get_time_pass(d->t_start, &(d->err)), philo->id, "has taken a fork 2", d);
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
- [[if_philo_b0d3c659|take_fork.c:57]] (ft_take_fork)
- [[if_philo_9f1639c7|take_fork.c:80]] (ft_take_fork)
- [[if_philo_4b75acf8|take_fork.c:45]] (ft_take_fork)

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
