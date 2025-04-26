---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: m_menu.c
line: 158
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `m_menu.c`
- **Ligne**: 158
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct menu_s
{
    short		numitems;	// # of menu items
    struct menu_s*	prevMenu;	// previous menu
    menuitem_t*		menuitems;	// menu items
    void		(*routine)();	// draw routine
    short		x;
    short		y;		// x,y of menu
    short		lastOn;		// last item user was on in menu
} menu_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_4a68f128|doomdata.h:153]] (global)
- [[typedef_struct_DOOM_a84704a0|r_defs.h:356]] (global)
- [[typedef_struct_DOOM_693f5e99|z_zone.h:58]] (global)
- [[typedef_struct_DOOM_57ba9303|wi_stuff.c:134]] (global)
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
