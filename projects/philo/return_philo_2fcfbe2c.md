---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: time.c
line: 21
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `time.c`
- **Ligne**: 21
- **Fonction**: get_time_pass
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (*error = 5, 0);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_61bbc82c|parsing.c:21]] (ft_atoi)
- [[return_philo_7dba8062|parsing.c:27]] (ft_atoi)
- [[return_philo_7dba8062|parsing.c:27]] (ft_atoi)
- [[return_philo_2ca8faf0|parsing.c:27]] (ft_atoi)
- [[return_philo_2ca8faf0|parsing.c:27]] (ft_atoi)

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
