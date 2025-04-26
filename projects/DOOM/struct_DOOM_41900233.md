---
tags: pattern, pattern/struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: struct
pattern_variant: simple
source_file: m_menu.c
line: 158
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 📐 Plan d'assemblage (STRUCT) (Simple)

## Contexte
- **Fichier**: `m_menu.c`
- **Ligne**: 158
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
📐 **Plan d'assemblage**

Comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.

## Code Source
```c
struct menu_s
{
    short		numitems;	// # of menu items
    struct menu_s*	prevMenu;	// previous menu
    menuitem_t*		menuitems;	// menu items
    void		(*routine)();	// draw routine
    short		x;
    short		y;		// x,y of menu
    short		lastOn;		// last item user was on in menu
}
```

## Note Factorio-style
*Ce pattern fonctionne comme plan d'assemblage dans Factorio. Il comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.*

## Patterns Similaires
- [[struct_DOOM_e4d39736|z_zone.h:58]] (global)
- [[struct_DOOM_db7dcab1|p_mobj.h:207]] (global)
- [[struct_DOOM_0e5ca5aa|r_defs.h:179]] (global)

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
