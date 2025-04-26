---
tags: pattern, pattern/enum, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: enum
pattern_variant: simple
source_file: p_spec.h
line: 262
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔢 Palette de ressources (ENUM) (Simple)

## Contexte
- **Fichier**: `p_spec.h`
- **Ligne**: 262
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
    up,
    down,
    waiting,
    in_stasis

}
```

## Note Factorio-style
*Ce pattern fonctionne comme palette de ressources dans Factorio. Il comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.*

## Patterns Similaires
- [[enum_DOOM_46efc6b0|p_spec.h:397]] (global)
- [[enum_DOOM_f6e681ce|p_spec.h:602]] (global)
- [[enum_DOOM_aa340874|p_spec.h:218]] (global)
- [[enum_DOOM_2eadd584|soundst.h:150]] (global)

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
