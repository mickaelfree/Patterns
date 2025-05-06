---
tags: pattern, pattern/struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: struct
pattern_variant: simple
source_file: philo.h
line: 59
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 📐 Plan d'assemblage (STRUCT) (Simple)

## Contexte
- **Fichier**: `philo.h`
- **Ligne**: 59
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
📐 **Plan d'assemblage**

Comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.

## Code Source
```c
struct s_table
{
	time_t			start_time;
	unsigned int	nb_philos;
	pthread_t		grim_reaper;
	time_t			time_to_die;
	time_t			time_to_eat;
	time_t			time_to_sleep;
	int				must_eat_count;
	bool			sim_stop;
	pthread_mutex_t	sim_stop_lock;
	pthread_mutex_t	write_lock;
	pthread_mutex_t	*fork_locks;
	t_philo			**philos;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme plan d'assemblage dans Factorio. Il comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.*

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
