---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: ipc.c
line: 77
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `ipc.c`
- **Ligne**: 77
- **Fonction**: init_philo_ipc
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_philo_ipc(t_table *table, t_philo *philo)
{
	if (table->nb_philos == 1)
		return ;
	sem_unlink(philo->sem_meal_name);
	if (!philo_open_global_semaphores(philo))
		child_exit(table, CHILD_EXIT_ERR_SEM);
	if (!philo_open_local_semaphores(philo))
		child_exit(table, CHILD_EXIT_ERR_SEM);
	if (pthread_create(&philo->personal_grim_reaper, NULL,
			&personal_grim_reaper, table) != 0)
		child_exit(table, CHILD_EXIT_ERR_PTHREAD);
	return ;
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
