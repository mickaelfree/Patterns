---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: p_spec.h
line: 165
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `p_spec.h`
- **Ligne**: 165
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct
{
    thinker_t	thinker;
    sector_t*	sector;
    int		minlight;
    int		maxlight;
    int		direction;

} glow_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_06bf16e7|p_spec.h:124]] (global)
- [[typedef_struct_DOOM_cb57c4cd|p_spec.h:150]] (global)
- [[typedef_struct_DOOM_d2201af9|p_spec.h:136]] (global)
- [[typedef_struct_DOOM_74692a37|p_spec.h:493]] (global)
- [[typedef_struct_DOOM_e4fea1fa|p_spec.h:343]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
*Aucun pattern lié trouvé*
