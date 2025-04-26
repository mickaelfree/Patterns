---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/nested
date: 2025-04-25
pattern_type: if
pattern_variant: nested
source_file: memory_manager.c
line: 48
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 48
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
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
```

## Analyse Structurelle
**Type détecté**: Capteur en cascade

Ces capteurs en cascade pourraient être combinés en un seul réseau logique avec des opérateurs && ou ||.

**Analogie Factorio**:
Comme plusieurs capteurs en série dans Factorio que vous pourriez remplacer par un circuit combinatoire unique.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_fdf_e585eb1f|memory_manager.c:94]] (my_free)
- [[if_fdf_af08ab7d|memory_manager.c:227]] (print_memory_map)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_fdf_1041c8ff|🔀 Répartiteur alternatif (ELSE)]]
[[else_fdf_16c235a8|🔀 Répartiteur alternatif (ELSE)]]
