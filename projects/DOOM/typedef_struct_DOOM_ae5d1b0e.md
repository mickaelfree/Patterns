---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: p_spec.h
line: 227
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `p_spec.h`
- **Ligne**: 227
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
    line_t*	line;
    bwhere_e	where;
    int		btexture;
    int		btimer;
    mobj_t*	soundorg;

} button_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_360d96a9|r_defs.h:460]] (global)
- [[typedef_struct_DOOM_ac21d740|p_spec.c:60]] (global)
- [[typedef_struct_DOOM_5d44f821|w_wad.h:56]] (global)
- [[typedef_struct_DOOM_1e94cc9c|d_items.h:34]] (global)
- [[typedef_struct_DOOM_5f29e372|p_spec.h:418]] (global)

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
