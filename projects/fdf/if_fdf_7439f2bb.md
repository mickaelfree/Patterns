---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: if
pattern_variant: simple
source_file: memory_manager.c
line: 150
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🔍 Capteur logique (IF) (Capteur simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 150
- **Fonction**: print_memory_content
- **Projet**: fdf
- **Variante**: Capteur simple
- **Complexité**: standard

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
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
```

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

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
