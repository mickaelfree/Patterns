---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: typedef struct
pattern_variant: simple
source_file: philo_bonus.h
line: 99
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `philo_bonus.h`
- **Ligne**: 99
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct s_philo
{
	pthread_t			personal_grim_reaper;
	sem_t				*sem_forks;
	sem_t				*sem_write;
	sem_t				*sem_philo_full;
	sem_t				*sem_philo_dead;
	sem_t				*sem_meal;
	char				*sem_meal_name;
	unsigned int		nb_forks_held;
	unsigned int		id;
	unsigned int		times_ate;
	bool				ate_enough;
	time_t				last_meal;
	t_table				*table;
}	t_philo;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_philo_8976cf5d|philo.h:75]] (global)

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
