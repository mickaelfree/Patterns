---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: simulation_bonus.c
line: 52
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `simulation_bonus.c`
- **Ligne**: 52
- **Fonction**: philo_routine
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	philo_routine(t_philo *philo)
{
	sem_wait(philo->sems->fork_sem);
	print_action(philo, "has taken a fork");
	sem_wait(philo->sems->fork_sem);
	print_action(philo, "has taken a fork");
	print_action(philo, "is eating");
	sem_wait(philo->sems->die_sem);
	philo->times.last_meal = get_current_time();
	philo->meals_eaten += 1;
	sem_post(philo->sems->die_sem);
	if (philo->meals_eaten >= philo->must_eat)
		sem_post(philo->sems->meal_sem);
	ft_usleep(philo->times.eat);
	sem_post(philo->sems->fork_sem);
	sem_post(philo->sems->fork_sem);
	print_action(philo, "is sleeping");
	ft_usleep(philo->times.sleep);
	print_action(philo, "is thinking");
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
