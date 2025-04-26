---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: memory_manager.c
line: 202
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 202
- **Fonction**: inspect_allocated_block
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
ensemble complète de notre pool mémoire
void print_memory_map() {
    if (memory_pool == NULL || first_block == NULL) {
        printf("Pool mémoire non initialisé.\n");
        return;
    }
    
    printf("\n====== CARTE MÉMOIRE COMPLÈTE ======\n");
    printf("Pool mémoire: début à %p, taille totale %d octets\n\n", 
           memory_pool, MEMORY_SIZE);
    
    Block *current = first_block;
    size_t total_free = 0;
    size_t total_used = 0;
    int block_count = 0;
    
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
    
    printf("\nRécapitulatif:\n");
    printf("  - Nombre total de blocs: %d\n", block_count);
    printf("  - Mémoire utilisée: %zu octets (%.2f%%)\n", 
           total_used, (float)total_used / MEMORY_SIZE * 100);
    printf("  - Mémoire libre: %zu octets (%.2f%%)\n", 
           total_free, (float)total_free / MEMORY_SIZE * 100);
    printf("====================================\n\n");
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_fdf_2a890ee3|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_3fed850e|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_b83d5c36|🚚 Convoyeur de sortie (RETURN)]]
