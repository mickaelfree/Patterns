---
tags: pattern, pattern/enum, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: enum
pattern_variant: simple
source_file: f_wipe.h
line: 30
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔢 Palette de ressources (ENUM) (Simple)

## Contexte
- **Fichier**: `f_wipe.h`
- **Ligne**: 30
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
    // simple gradual pixel change for 8-bit only
    wipe_ColorXForm,
    
    // weird screen melt
    wipe_Melt,	

    wipe_NUMWIPES
}
```

## Note Factorio-style
*Ce pattern fonctionne comme palette de ressources dans Factorio. Il comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.*

## Patterns Similaires
- [[enum_DOOM_941e2311|d_event.h:72]] (global)
- [[enum_DOOM_f9be9e8d|d_player.h:53]] (global)
- [[enum_DOOM_0408050d|d_player.h:68]] (global)
- [[enum_DOOM_4202caf4|p_mobj.h:117]] (global)
- [[enum_DOOM_6c5a058f|p_spec.h:537]] (global)

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
