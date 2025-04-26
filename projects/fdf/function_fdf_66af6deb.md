---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: memory_manager.c
line: 80
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 80
- **Fonction**: my_free
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
personnalisée
void my_free(void *ptr) {
    if (ptr == NULL) return;
    
    // Récupération de l'en-tête du bloc
    Block *block = (Block *)((char *)ptr - sizeof(Block));
    
    // Marquer le bloc comme libre
    block->is_free = 1;
    
    // Fusion des blocs libres adjacents
    Block *current = first_block;
    
    while (current != NULL && current->next != NULL) {
        if (current->is_free && current->next->is_free) {
            // Fusion avec le bloc suivant
            current->size += sizeof(Block) + current->next->size;
            current->next = current->next->next;
            // Pas d'incrémentation de current ici car on veut vérifier
            // si on peut fusionner plusieurs blocs consécutifs
        } else {
            current = current->next;
        }
    }
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
