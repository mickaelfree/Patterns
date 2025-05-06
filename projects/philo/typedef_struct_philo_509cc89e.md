---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: typedef struct
pattern_variant: simple
source_file: philo.h
line: 29
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `philo.h`
- **Ligne**: 29
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct s_mutexes
{
	t_mutex	*left_fork;
	t_mutex	*right_fork;
	t_mutex	*write_lock;
	t_mutex	*meal_lock;
}	t_mutexes;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_philo_d089f551|philo.h:57]] (global)
- [[typedef_struct_philo_79a2d728|struct.h:37]] (global)
- [[typedef_struct_philo_79a2d728|struct.h:37]] (global)
- [[typedef_struct_philo_79a2d728|struct.h:37]] (global)
- [[typedef_struct_philo_79a2d728|struct.h:37]] (global)

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
