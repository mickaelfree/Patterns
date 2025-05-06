---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: exit.c
line: 56
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `exit.c`
- **Ligne**: 56
- **Fonction**: child_exit
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	child_exit(t_table *table, int exit_code)
{
	sem_post(table->this_philo->sem_meal);
	pthread_join(table->this_philo->personal_grim_reaper, NULL);
	if (exit_code == CHILD_EXIT_ERR_SEM)
		msg(STR_ERR_SEM, NULL, 0);
	if (exit_code == CHILD_EXIT_ERR_PTHREAD)
		msg(STR_ERR_THREAD, NULL, 0);
	sem_close(table->this_philo->sem_forks);
	sem_close(table->this_philo->sem_philo_full);
	sem_close(table->this_philo->sem_philo_dead);
	sem_close(table->this_philo->sem_write);
	sem_close(table->this_philo->sem_meal);
	free_table(table);
	exit(exit_code);
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
