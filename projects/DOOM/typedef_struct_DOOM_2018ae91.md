---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: p_local.h
line: 144
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `p_local.h`
- **Ligne**: 144
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
    fixed_t	frac;		// along trace line
    boolean	isaline;
    union {
	mobj_t*	thing;
	line_t*	line;
    }			d;
} intercept_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_6526082d|d_player.h:187]] (global)
- [[typedef_struct_DOOM_20449c1d|p_pspr.h:68]] (global)
- [[typedef_struct_DOOM_89e38f3e|r_defs.h:88]] (global)
- [[typedef_struct_DOOM_14e71eba|am_map.c:138]] (global)
- [[typedef_struct_DOOM_57ba9303|wi_stuff.c:134]] (global)

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
