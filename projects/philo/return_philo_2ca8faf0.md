---
tags: pattern, pattern/return, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: return
pattern_variant: simple
source_file: init_parsing.c
line: 31
project: philo
first_seen: 2025-05-07
occurrences: 14
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `init_parsing.c`
- **Ligne**: 31
- **Fonction**: ft_atoi
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (*error = 4, 0);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_philo_61bbc82c|parsing.c:21]] (ft_atoi)
- [[return_philo_7dba8062|parsing.c:27]] (ft_atoi)
- [[return_philo_2fcfbe2c|time.c:26]] (get_time_pass)
- [[return_philo_7dba8062|parsing.c:27]] (ft_atoi)
- [[return_philo_2fcfbe2c|time.c:26]] (get_time_pass)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 14 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_philo_5ee0ee7c|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_f59e1634|🏭 Usine modulaire (FUNCTION)]]
[[function_philo_7916a54f|🏭 Usine modulaire (FUNCTION)]]
