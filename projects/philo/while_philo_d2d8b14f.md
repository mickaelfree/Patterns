---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: while
pattern_variant: simple
source_file: grim_reaper.c
line: 49
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `grim_reaper.c`
- **Ligne**: 49
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (table->philo_full_count < table->nb_philos)
	{
		if (has_simulation_stopped(table) == true)
			return (NULL);
		sem_wait(table->sem_philo_full);
		if (has_simulation_stopped(table) == false)
			table->philo_full_count += 1;
		else
			return (NULL);
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
*Aucun pattern lié trouvé*
