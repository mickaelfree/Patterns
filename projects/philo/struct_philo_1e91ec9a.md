---
tags: pattern, pattern/struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: struct
pattern_variant: simple
source_file: philo.h
line: 75
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 📐 Plan d'assemblage (STRUCT) (Simple)

## Contexte
- **Fichier**: `philo.h`
- **Ligne**: 75
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
📐 **Plan d'assemblage**

Comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.

## Code Source
```c
struct s_philo
{
	pthread_t			thread;
	unsigned int		id;
	unsigned int		times_ate;
	unsigned int		fork[2];
	pthread_mutex_t		meal_time_lock;
	time_t				last_meal;
	t_table				*table;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme plan d'assemblage dans Factorio. Il comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.*

## Patterns Similaires
- [[struct_philo_893626ca|struct.h:20]] (global)
- [[struct_philo_893626ca|struct.h:20]] (global)
- [[struct_philo_893626ca|struct.h:20]] (global)
- [[struct_philo_893626ca|struct.h:20]] (global)

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
