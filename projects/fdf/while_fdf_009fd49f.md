---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: memory_manager.c
line: 218
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 218
- **Fonction**: print_memory_map
- **Projet**: fdf
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (current != NULL) {
        size_t block_total_size = sizeof(Block) + current->size;
        printf("Bloc %d: %p - %p (%zu octets) [%s]\n", 
               block_count++,
               (void*)current, 
               (void*)((char*)current + block_total_size - 1),
               block_total_size,
               current->is_free ? "LIBRE" : "OCCUPÉ");
        
        if (current->is_free) {
            total_free += block_total_size;
        } else {
            total_used += block_total_size;
        }
        
        current = current->next;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_fdf_c6b2ac6e|memory_manager.c:251]] (print_memory_state)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[for_fdf_aa045c10|🔄 Chaîne de montage (FOR)]]
[[for_fdf_b3efebf6|🔄 Chaîne de montage (FOR)]]
[[for_fdf_c97cbea4|🔄 Chaîne de montage (FOR)]]
