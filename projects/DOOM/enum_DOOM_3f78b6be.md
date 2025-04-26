---
tags: pattern, pattern/enum, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: enum
pattern_variant: simple
source_file: p_saveg.c
line: 220
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔢 Palette de ressources (ENUM) (Simple)

## Contexte
- **Fichier**: `p_saveg.c`
- **Ligne**: 220
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔢 **Palette de ressources**

Comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.

## Code Source
```c
enum
{
    tc_end,
    tc_mobj

}
```

## Note Factorio-style
*Ce pattern fonctionne comme palette de ressources dans Factorio. Il comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.*

## Patterns Similaires
- [[enum_DOOM_a109ca01|sounds.c:42]] (global)
- [[enum_DOOM_8db2683c|d_net.h:51]] (global)
- [[enum_DOOM_f6e681ce|p_spec.h:602]] (global)
- [[enum_DOOM_aa340874|p_spec.h:218]] (global)
- [[enum_DOOM_72c66bf4|doomtype.h:34]] (global)

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
