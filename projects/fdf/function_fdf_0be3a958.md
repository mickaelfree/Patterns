---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: memory_manager.c
line: 116
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 116
- **Fonction**: print_memory_content
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void print_memory_content(void *start, size_t length) {
    unsigned char *ptr = (unsigned char *)start;
    
    printf("Contenu mémoire à l'adresse %p (taille: %zu octets):\n", start, length);
    
    // Affichage de l'en-tête
    printf("         | 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F | ASCII\n");
    printf("---------+-------------------------------------------------+-----------------\n");
    
    // Nombre de lignes complètes à afficher
    size_t full_lines = length / 16;
    
    // Pour chaque ligne de 16 octets
    for (size_t i = 0; i < full_lines; i++) {
        printf("%08zX | ", i * 16);
        
        // Affichage hexadécimal
        for (size_t j = 0; j < 16; j++) {
            printf("%02X ", ptr[i * 16 + j]);
        }
        
        printf("| ");
        
        // Affichage ASCII
        for (size_t j = 0; j < 16; j++) {
            unsigned char c = ptr[i * 16 + j];
            printf("%c", (c >= 32 && c <= 126) ? c : '.'); // Caractères imprimables uniquement
        }
        
        printf("\n");
    }
    
    // Afficher les octets restants s'il y en a
    size_t remaining = length % 16;
    if (remaining > 0) {
        printf("%08zX | ", full_lines * 16);
        
        // Affichage hexadécimal des octets restants
        for (size_t j = 0; j < remaining; j++) {
            printf("%02X ", ptr[full_lines * 16 + j]);
        }
        
        // Remplir avec des espaces pour aligner la partie ASCII
        for (size_t j = remaining; j < 16; j++) {
            printf("   ");
        }
        
        printf("| ");
        
        // Affichage ASCII des octets restants
        for (size_t j = 0; j < remaining; j++) {
            unsigned char c = ptr[full_lines * 16 + j];
            printf("%c", (c >= 32 && c <= 126) ? c : '.');
        }
        
        printf("\n");
    }
    
    printf("---------+-------------------------------------------------+-----------------\n");
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
