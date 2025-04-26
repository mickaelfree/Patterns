---
tags: pattern, pattern/return, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: return
pattern_variant: simple
source_file: get_next_line_utils.c
line: 57
project: fdf
first_seen: 2025-04-25
occurrences: 12
ai_analyzed: non
optimizable: non
---

# 🚚 Convoyeur de sortie (RETURN) (Simple)

## Contexte
- **Fichier**: `get_next_line_utils.c`
- **Ligne**: 57
- **Fonction**: ft_strlen
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🚚 **Convoyeur de sortie**

Comme un convoyeur qui renvoie le produit fini hors de l'usine.

## Code Source
```c
return (str - start + 3);
```

## Note Factorio-style
*Ce pattern fonctionne comme convoyeur de sortie dans Factorio. Il comme un convoyeur qui renvoie le produit fini hors de l'usine.*

## Patterns Similaires
- [[return_fdf_9dc37e69|get_next_line.c:45]] (ft_find_newline)
- [[return_fdf_a98cfb70|get_next_line.c:49]] (ft_find_newline)
- [[return_fdf_9dc37e69|get_next_line.c:45]] (ft_find_newline)
- [[return_fdf_a98cfb70|get_next_line.c:49]] (ft_find_newline)
- [[return_fdf_b80353c7|get_next_line.c:41]] (ft_find_newline)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 12 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[function_fdf_7c9786dd|🏭 Usine modulaire (FUNCTION)]]
[[function_fdf_19fe2041|🏭 Usine modulaire (FUNCTION)]]
[[function_fdf_5d89438a|🏭 Usine modulaire (FUNCTION)]]
