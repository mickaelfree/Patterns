---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init.c
line: 107
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init.c`
- **Ligne**: 107
- **Fonction**: init_global_semaphores
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static bool	init_global_semaphores(t_table *table)
{
	unlink_global_sems();
	table->sem_forks = sem_open(SEM_NAME_FORKS, O_CREAT,
			S_IRUSR | S_IWUSR, table->nb_philos);
	if (table->sem_forks == SEM_FAILED)
		return (sem_error_cleanup(table));
	table->sem_write = sem_open(SEM_NAME_WRITE, O_CREAT,
			S_IRUSR | S_IWUSR, 1);
	if (table->sem_write == SEM_FAILED)
		return (sem_error_cleanup(table));
	table->sem_philo_full = sem_open(SEM_NAME_FULL, O_CREAT,
			S_IRUSR | S_IWUSR, table->nb_philos);
	if (table->sem_philo_full == SEM_FAILED)
		return (sem_error_cleanup(table));
	table->sem_philo_dead = sem_open(SEM_NAME_DEAD, O_CREAT,
			S_IRUSR | S_IWUSR, table->nb_philos);
	if (table->sem_philo_dead == SEM_FAILED)
		return (sem_error_cleanup(table));
	table->sem_stop = sem_open(SEM_NAME_STOP, O_CREAT,
			S_IRUSR | S_IWUSR, 1);
	if (table->sem_stop == SEM_FAILED)
		return (sem_error_cleanup(table));
	return (true);
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
