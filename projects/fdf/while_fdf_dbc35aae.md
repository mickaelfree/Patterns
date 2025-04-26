---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: memory_manager.c
line: 47
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 47
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (current != NULL) {
        if (current->is_free && current->size >= size) {
            // On a trouvé un bloc libre assez grand
            
            // Si le bloc est significativement plus grand que ce dont on a besoin,
            // on le divise en deux
            if (current->size >= size + sizeof(Block) + 8) {
                // Création d'un nouveau bloc après notre allocation
                new_block = (Block *)((char *)current + sizeof(Block) + size);
                new_block->size = current->size - size - sizeof(Block);
                new_block->is_free = 1;
                new_block->next = current->next;
                
                // Mise à jour du bloc courant
                current->size = size;
                current->next = new_block;
            }
            
            // Marquer le bloc comme occupé
            current->is_free = 0;
            
            // Le pointeur à retourner est juste après l'en-tête du bloc
            result = (void *)((char *)current + sizeof(Block));
            break;
        }
        
        previous = current;
        current = current->next;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_fdf_0192158f|memory_manager.c:93]] (my_free)

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
