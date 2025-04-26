---
tags: pattern, pattern/return, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: fdf.c
line: 61
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 61
- **Fonction**: ft_atoi_base
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (result * sign);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_fdf_fb179552|memory_manager.c:77]] (global)
- [[return_fdf_df45ddab|get_next_line.c:28]] (global)
- [[return_fdf_df45ddab|get_next_line.c:28]] (global)
- [[return_fdf_63aaece2|fdf.c:84]] (get_height)
- [[return_fdf_d183ade1|split.c:26]] (ft_strlcpy)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_fdf_7c9786dd|🏭 Usine modulaire (FUNCTION)]]
[[function_fdf_19fe2041|🏭 Usine modulaire (FUNCTION)]]
[[function_fdf_5d89438a|🏭 Usine modulaire (FUNCTION)]]
