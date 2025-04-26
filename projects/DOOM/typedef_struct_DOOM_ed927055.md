---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: doomdata.h
line: 180
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `doomdata.h`
- **Ligne**: 180
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
  // Partition line from (x,y) to x+dx,y+dy)
  short		x;
  short		y;
  short		dx;
  short		dy;

  // Bounding box for each child,
  // clip against view frustum.
  short		bbox[2][4];

  // If NF_SUBSECTOR its a subsector,
  // else it's a node of another subtree.
  unsigned short	children[2];

} mapnode_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_954865b5|m_menu.c:140]] (global)
- [[typedef_struct_DOOM_36d666d0|r_data.c:99]] (global)
- [[typedef_struct_DOOM_43a05cbe|r_data.c:113]] (global)
- [[typedef_struct_DOOM_fcc255a6|s_sound.c:93]] (global)
- [[typedef_struct_DOOM_2da90e74|z_zone.c:46]] (global)

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
