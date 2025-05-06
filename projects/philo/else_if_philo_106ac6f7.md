---
tags: pattern, pattern/else-if, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: else if
pattern_variant: simple
source_file: message.c
line: 27
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Répartiteur intelligent (ELSE IF) (Filtrage simple)

## Contexte
- **Fichier**: `message.c`
- **Ligne**: 27
- **Fonction**: ft_message
- **Projet**: philo
- **Variante**: Filtrage simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Répartiteur intelligent**

Comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.

## Code Source
```c
else if (d->evryone_is_alive == TRUE && !d->err)
	{
		pthread_mutex_unlock(mutexs.check);
		pthread_mutex_lock(mutexs.use_printf);
		if (d->one_dead == FALSE)
			printf("%ld %d %s\n", time, philo->id + 1, message);
		pthread_mutex_unlock(mutexs.use_printf);
		return ;
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur intelligent dans Factorio. Il comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[if_philo_bf2fef7e|🔍 Capteur logique (IF)]]
[[if_philo_d9e68386|🔍 Capteur logique (IF)]]
[[if_philo_a0812442|🔍 Capteur logique (IF)]]
