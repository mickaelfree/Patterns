---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: info.h
line: 1147
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `info.h`
- **Ligne**: 1147
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
  spritenum_t	sprite;
  long			frame;
  long			tics;
  // void		(*action) ();
  actionf_t			action;
  statenum_t			nextstate;
  long			misc1, misc2;
} state_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_4a68f128|doomdata.h:153]] (global)
- [[typedef_struct_DOOM_57ba9303|wi_stuff.c:134]] (global)
- [[typedef_struct_DOOM_95ab75fc|d_event.h:44]] (global)
- [[typedef_struct_DOOM_20449c1d|p_pspr.h:68]] (global)
- [[typedef_struct_DOOM_ca139b7e|am_map.c:148]] (global)

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
