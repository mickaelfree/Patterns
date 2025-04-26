---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: p_spec.h
line: 343
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `p_spec.h`
- **Ligne**: 343
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
    vldoor_e	type;
    sector_t*	sector;
    fixed_t	topheight;
    fixed_t	speed;

    // 1 = up, 0 = waiting at top, -1 = down
    int             direction;
    
    // tics to wait at the top
    int             topwait;
    // (keep in case a door going down is reset)
    // when it reaches 0, start going down
    int             topcountdown;
    
} vldoor_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_74692a37|p_spec.h:493]] (global)
- [[typedef_struct_DOOM_db330ac5|p_spec.h:584]] (global)
- [[typedef_struct_DOOM_06bf16e7|p_spec.h:124]] (global)
- [[typedef_struct_DOOM_bc23c694|p_spec.h:165]] (global)
- [[typedef_struct_DOOM_cb57c4cd|p_spec.h:150]] (global)

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
