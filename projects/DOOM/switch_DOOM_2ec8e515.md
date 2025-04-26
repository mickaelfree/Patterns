---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/fallthrough
date: 2025-04-25
pattern_type: switch
pattern_variant: fallthrough
source_file: hu_stuff.c
line: 446
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Aiguillage multiple (SWITCH) (Fallthrough)

## Contexte
- **Fichier**: `hu_stuff.c`
- **Ligne**: 446
- **Fonction**: HU_Start
- **Projet**: DOOM
- **Variante**: Fallthrough
- **Complexité**: avancée

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch ( gamemode )
    {
      case shareware:
      case registered:
      case retail:
	s = HU_TITLE;
	break;

/* FIXME
      case pack_plut:
	s = HU_TITLEP;
	break;
      case pack_tnt:
	s = HU_TITLET;
	break;
*/
	
      case commercial:
      default:
	 s = HU_TITLE2;
	 break;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

## Patterns Similaires
- [[switch_DOOM_bd5ca9a4|p_ceilng.c:149]] (global)
- [[switch_DOOM_bd72bb46|m_menu.c:779]] (M_DrawReadThis2)
- [[switch_DOOM_058d1b17|g_game.c:1156]] (G_WorldDone)
- [[switch_DOOM_146d21e6|g_game.c:1078]] (if)
- [[switch_DOOM_b30c4920|g_game.c:1072]] (if)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
