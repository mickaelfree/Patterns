---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: init.c
line: 129
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `init.c`
- **Ligne**: 129
- **Fonction**: init_global_semaphores
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (sem_error_cleanup(table));
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_9b9b3daf|main.c:145]] (main)
- [[return_philo_44eac3c9|main.c:148]] (main)
- [[return_philo_093beae5|main.c:31]] (start_simulation)
- [[return_philo_093beae5|main.c:31]] (start_simulation)
- [[return_philo_093beae5|main.c:31]] (start_simulation)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 5 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_philo_5ee0ee7c|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_f59e1634|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_7916a54f|🏭 Usine modulaire (FUNCTION)]]
