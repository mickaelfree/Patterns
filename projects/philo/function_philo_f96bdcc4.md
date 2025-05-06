---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_bonus.c
line: 42
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_bonus.c`
- **Ligne**: 42
- **Fonction**: init_philos
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_sems(t_engine *engine, t_sems *sems, int count)
{
	sems->die_sem = sem_open(DIE_SEM_NAME, O_CREAT | O_EXCL, 0644, 1);
	sems->fork_sem = sem_open(FORK_SEM_NAME, O_CREAT | O_EXCL, 0644, count);
	sems->meal_sem = sem_open(MEAL_SEM_NAME, O_CREAT | O_EXCL, 0644, 0);
	sems->write_sem = sem_open(WRITE_SEM_NAME, O_CREAT | O_EXCL, 0644, 1);
	if (sems->die_sem == SEM_FAILED || sems->fork_sem == SEM_FAILED
		|| sems->meal_sem == SEM_FAILED || sems->write_sem == SEM_FAILED)
		destroy_all(engine, "[Semaphore Open ERROR]\n", true, EXIT_FAILURE);
	if (sem_unlink(DIE_SEM_NAME) == -1 || sem_unlink(FORK_SEM_NAME) == -1
		|| sem_unlink(MEAL_SEM_NAME) == -1 || sem_unlink(WRITE_SEM_NAME) == -1)
		destroy_all(engine, "[Semaphore Unlink ERROR]\n", true, EXIT_FAILURE);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
