---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: cleanup.c
line: 60
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `cleanup.c`
- **Ligne**: 60
- **Fonction**: sem_error_cleanup
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (error_failure(STR_ERR_SEM, NULL, table));
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_9fb9056d|init.c:111]] (init_global_mutexes)
- [[return_philo_9fb9056d|init.c:111]] (init_global_mutexes)
- [[return_philo_093beae5|main.c:31]] (start_simulation)
- [[return_philo_093beae5|main.c:31]] (start_simulation)
- [[return_philo_093beae5|main.c:31]] (start_simulation)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_philo_5ee0ee7c|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_f59e1634|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_7916a54f|🏭 Usine modulaire (FUNCTION)]]
