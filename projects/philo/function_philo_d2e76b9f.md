---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: utils_bonus.c
line: 22
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `utils_bonus.c`
- **Ligne**: 22
- **Fonction**: error_message
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	destroy_all(t_engine *engine, char *str, bool isParentProc, int signal)
{
	int	i;

	i = -1;
	if (isParentProc)
	{
		while (++i < engine->philo_count)
			if (engine->proc_ids[i] != -1)
				kill(engine->proc_ids[i], SIGKILL);
	}
	if (engine->sems->die_sem != SEM_FAILED)
		sem_close(engine->sems->die_sem);
	if (engine->sems->fork_sem != SEM_FAILED)
		sem_close(engine->sems->fork_sem);
	if (engine->sems->meal_sem != SEM_FAILED)
		sem_close(engine->sems->meal_sem);
	if (engine->sems->write_sem != SEM_FAILED)
		sem_close(engine->sems->write_sem);
	i = -1;
	while (++i < engine->philo_count)
		free(engine->philos[i]);
	free(engine->sems);
	free(engine->philos);
	free(engine->proc_ids);
	free(engine);
	error_message(str, signal);
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
