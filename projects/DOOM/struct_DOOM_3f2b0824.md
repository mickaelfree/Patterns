---
tags: pattern, pattern/struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: struct
pattern_variant: simple
source_file: r_defs.h
line: 375
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 📐 Plan d'assemblage (STRUCT) (Simple)

## Contexte
- **Fichier**: `r_defs.h`
- **Ligne**: 375
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
📐 **Plan d'assemblage**

Comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.

## Code Source
```c
struct vissprite_s
{
    // Doubly linked list.
    struct vissprite_s*	prev;
    struct vissprite_s*	next;
    
    int			x1;
    int			x2;

    // for line side calculation
    fixed_t		gx;
    fixed_t		gy;		

    // global bottom / top for silhouette clipping
    fixed_t		gz;
    fixed_t		gzt;

    // horizontal position of x1
    fixed_t		startfrac;
    
    fixed_t		scale;
    
    // negative if flipped
    fixed_t		xiscale;	

    fixed_t		texturemid;
    int			patch;

    // for color translation and shadow draw,
    //  maxbright frames as well
    lighttable_t*	colormap;
   
    int			mobjflags;
    
}
```

## Note Factorio-style
*Ce pattern fonctionne comme plan d'assemblage dans Factorio. Il comme un plan qui définit comment assembler différentes pièces pour créer un élément complexe.*

## Patterns Similaires
- [[struct_DOOM_0e5ca5aa|r_defs.h:179]] (global)
- [[struct_DOOM_db7dcab1|p_mobj.h:207]] (global)
- [[struct_DOOM_254a931c|soundsrv.c:63]] (global)
- [[struct_DOOM_37286661|sounds.h:32]] (global)
- [[struct_DOOM_ae08dc42|soundst.h:94]] (global)

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
