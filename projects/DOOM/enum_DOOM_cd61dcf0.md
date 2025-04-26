---
tags: pattern, pattern/enum, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: enum
pattern_variant: simple
source_file: doomdef.h
line: 51
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔢 Palette de ressources (ENUM) (Simple)

## Contexte
- **Fichier**: `doomdef.h`
- **Ligne**: 51
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
  doom,		// DOOM 1
  doom2,	// DOOM 2
  pack_tnt,	// TNT mission pack
  pack_plut,	// Plutonia pack
  none

}
```

## Note Factorio-style
*Ce pattern fonctionne comme palette de ressources dans Factorio. Il comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.*

## Patterns Similaires
- [[enum_DOOM_48a95708|p_spec.h:575]] (global)
- [[enum_DOOM_941e2311|d_event.h:72]] (global)
- [[enum_DOOM_f9be9e8d|d_player.h:53]] (global)
- [[enum_DOOM_0408050d|d_player.h:68]] (global)
- [[enum_DOOM_d979b1d6|doomdef.h:201]] (global)

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
