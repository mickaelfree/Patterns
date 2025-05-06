---
tags: pattern, pattern/struct, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: struct
pattern_variant: simple
source_file: philo_bonus.h
line: 59
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 📐 Plan d'assemblage (STRUCT) (Simple)

## Contexte
- **Fichier**: `philo_bonus.h`
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
struct s_philo
{
	int			id;
	t_sems		*sems;
	t_times		times;
	int			must_eat;
	int			meals_eaten;
	int			philo_count;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme plan d'assemblage dans Factorio. Il comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.*

## Patterns Similaires
- [[struct_philo_e35ce53d|philo.h:46]] (global)
- [[struct_philo_9ba0a9ce|philo_bonus.h:69]] (global)
- [[struct_philo_7068351e|struct.h:20]] (global)
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
