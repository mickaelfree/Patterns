---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: simulation.c
line: 45
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `simulation.c`
- **Ligne**: 45
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (true)
	{
		i = -1;
		while (++i < philos[0].philo_count)
		{
			pthread_mutex_lock(philos->mutexes.meal_lock);
			if (get_current_time() - philos[i].times.last_meal
				> philos[i].times.die)
			{
				pthread_mutex_unlock(philos->mutexes.meal_lock);
				print_action(&philos[i], RED" died"RESET);
				pthread_mutex_lock(philos->mutexes.write_lock);
				return (NULL);
			}
			pthread_mutex_unlock(philos->mutexes.meal_lock);
		}
		if (is_all_eat(philos))
			return (NULL);
	}
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_philo_6df29fbe|simulation.c:24]] (is_all_eat)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
*Aucun pattern lié trouvé*
