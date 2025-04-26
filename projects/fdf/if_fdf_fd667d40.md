---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: if
pattern_variant: simple
source_file: memory_manager.c
line: 204
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 204
- **Fonction**: print_memory_map
- **Projet**: fdf
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (memory_pool == NULL || first_block == NULL) {
        printf("Pool mémoire non initialisé.\n");
        return;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_fdf_dc259fa9|memory_manager.c:23]] (memory_init)
- [[if_fdf_0d063594|memory_manager.c:179]] (inspect_allocated_block)

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
