---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: if
pattern_variant: simple
source_file: memory_manager.c
line: 227
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 227
- **Fonction**: print_memory_map
- **Projet**: fdf
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (current->is_free) {
            total_free += block_total_size;
        }
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_fdf_feab5411|memory_manager.c:48]] (global)
- [[if_fdf_e585eb1f|memory_manager.c:94]] (my_free)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[else_fdf_1041c8ff|🔀 Répartiteur alternatif (ELSE)]]
[[else_fdf_16c235a8|🔀 Répartiteur alternatif (ELSE)]]
