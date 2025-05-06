---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: routine_and_fork.c
line: 48
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `routine_and_fork.c`
- **Ligne**: 48
- **Fonction**: is_finish
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (pthread_mutex_unlock(data->mutexs.check), 0);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_d3218fe2|routine_and_fork.c:46]] (is_finish)
- [[return_philo_d3218fe2|routine_and_fork.c:46]] (is_finish)
- [[return_philo_3d7c9daa|gestion_thread.c:19]] (someone_died)
- [[return_philo_3d7c9daa|gestion_thread.c:19]] (someone_died)
- [[return_philo_3d7c9daa|gestion_thread.c:19]] (someone_died)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_philo_5ee0ee7c|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_f59e1634|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_7916a54f|🏭 Usine modulaire (FUNCTION)]]
