---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: switch
pattern_variant: simple
source_file: p_plats.c
line: 154
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔀 Aiguillage multiple (SWITCH) (Simple)

## Contexte
- **Fichier**: `p_plats.c`
- **Ligne**: 154
- **Fonction**: EV_DoPlat
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch(type)
    {
      case perpetualRaise:
	P_ActivateInStasis(line->tag);
	break;
	
      default:
	break;
    }
```

## Analyse Structurelle
**Type détecté**: Simple

Cet aiguillage ne gère que 1 voies - un simple if/else serait plus efficace.

**Analogie Factorio**:
Comme un réseau ferroviaire complexe pour seulement 2 destinations - un simple répartiteur suffirait.

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

## Patterns Similaires
- [[switch_DOOM_6cde57d1|p_ceilng.c:185]] (EV_DoCeiling)
- [[switch_DOOM_bd5ca9a4|p_ceilng.c:149]] (global)
- [[switch_DOOM_146d21e6|g_game.c:1078]] (if)
- [[switch_DOOM_f9e4d3e4|p_floor.c:228]] (global)
- [[switch_DOOM_b30c4920|g_game.c:1072]] (if)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
