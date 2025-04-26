---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: wadread.c
line: 73
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `wadread.c`
- **Ligne**: 73
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct lumpinfo_struct
{
    int		handle;
    int		filepos;
    int		size;
    char	name[8];

} lumpinfo_t;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Patterns Similaires
- [[typedef_struct_DOOM_2b38308f|soundsrv.c:73]] (global)
- [[typedef_struct_DOOM_2b38308f|soundsrv.c:73]] (global)
- [[typedef_struct_DOOM_eabe932a|w_wad.h:45]] (global)
- [[typedef_struct_DOOM_5d44f821|w_wad.h:56]] (global)
- [[typedef_struct_DOOM_66f6716c|wadread.c:57]] (global)

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
