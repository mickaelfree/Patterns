---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: hu_lib.h
line: 81
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `hu_lib.h`
- **Ligne**: 81
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
    hu_textline_t	l;		// text line to input on

     // left margin past which I am not to delete characters
    int			lm;

    // pointer to boolean stating whether to update window
    boolean*		on; 
    boolean		laston; // last value of *->on;

} hu_itext_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_f1f5d6a9|hu_lib.h:65]] (global)
- [[typedef_struct_DOOM_aaf3655f|r_defs.h:179]] (global)
- [[typedef_struct_DOOM_6526082d|d_player.h:187]] (global)
- [[typedef_struct_DOOM_20449c1d|p_pspr.h:68]] (global)
- [[typedef_struct_DOOM_89e38f3e|r_defs.h:88]] (global)

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
