---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: init_data.c
line: 50
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `init_data.c`
- **Ligne**: 50
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (data->err = 3, data);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_c30fbd20|init_thread.c:43]] (on_or_off_all_thread)
- [[return_philo_21903520|init_thread.c:45]] (on_or_off_all_thread)
- [[return_philo_c30fbd20|init_thread.c:43]] (on_or_off_all_thread)
- [[return_philo_21903520|init_thread.c:45]] (on_or_off_all_thread)
- [[return_philo_f01c0439|init_data.c:28]] (global)

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
