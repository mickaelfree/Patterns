---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: typedef struct
pattern_variant: simple
source_file: philo_bonus.h
line: 59
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `philo_bonus.h`
- **Ligne**: 59
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
	int			id;
	t_sems		*sems;
	t_times		times;
	int			must_eat;
	int			meals_eaten;
	int			philo_count;
}	t_philo;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_philo_358f0284|philo.h:46]] (global)
- [[typedef_struct_philo_d3736f05|philo_bonus.h:69]] (global)
- [[typedef_struct_philo_2b6811ee|struct.h:20]] (global)
- [[typedef_struct_philo_551aa08b|struct.h:20]] (global)
- [[typedef_struct_philo_551aa08b|struct.h:20]] (global)

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
