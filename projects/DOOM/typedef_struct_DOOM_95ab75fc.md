---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: d_event.h
line: 44
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `d_event.h`
- **Ligne**: 44
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
    evtype_t	type;
    int		data1;		// keys / mouse/joystick buttons
    int		data2;		// mouse/joystick x move
    int		data3;		// mouse/joystick y move
} event_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_14e71eba|am_map.c:138]] (global)
- [[typedef_struct_DOOM_57ba9303|wi_stuff.c:134]] (global)
- [[typedef_struct_DOOM_1252a98b|f_finale.c:334]] (global)
- [[typedef_struct_DOOM_091decb1|r_defs.h:285]] (global)
- [[typedef_struct_DOOM_6526082d|d_player.h:187]] (global)

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
