---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: typedef struct
pattern_variant: simple
source_file: struct.h
line: 39
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `struct.h`
- **Ligne**: 39
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct s_all_mutex
{
	pthread_mutex_t	**all_fork;
	pthread_mutex_t	*use_printf;
	pthread_mutex_t	*eat;
	pthread_mutex_t	*check;
}	t_all_mutex;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_philo_509cc89e|philo.h:29]] (global)
- [[typedef_struct_philo_a31c8021|philo_bonus.h:42]] (global)
- [[typedef_struct_philo_8976cf5d|philo.h:75]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 5 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
*Aucun pattern lié trouvé*
