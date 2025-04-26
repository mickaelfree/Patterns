---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: p_pspr.h
line: 68
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `p_pspr.h`
- **Ligne**: 68
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
    state_t*	state;	// a NULL state means not active
    int		tics;
    fixed_t	sx;
    fixed_t	sy;

} pspdef_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_57ba9303|wi_stuff.c:134]] (global)
- [[typedef_struct_DOOM_89e38f3e|r_defs.h:88]] (global)
- [[typedef_struct_DOOM_2018ae91|p_local.h:144]] (global)
- [[typedef_struct_DOOM_1bb5316c|hu_lib.h:81]] (global)
- [[typedef_struct_DOOM_4a68f128|doomdata.h:153]] (global)

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
