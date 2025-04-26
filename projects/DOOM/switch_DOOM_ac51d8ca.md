---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/fallthrough
date: 2025-04-25
pattern_type: switch
pattern_variant: fallthrough
source_file: p_plats.c
line: 89
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Aiguillage multiple (SWITCH) (Fallthrough)

## Contexte
- **Fichier**: `p_plats.c`
- **Ligne**: 89
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Fallthrough
- **Complexité**: avancée

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch(plat->type)
		{
		  case blazeDWUS:
		  case downWaitUpStay:
		    P_RemoveActivePlat(plat);
		    break;
		    
		  case raiseAndChange:
		  case raiseToNearestAndChange:
		    P_RemoveActivePlat(plat);
		    break;
		    
		  default:
		    break;
		}
```

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

## Patterns Similaires
- [[switch_DOOM_b71c6369|p_inter.c:737]] (P_KillMobj)
- [[switch_DOOM_bd5ca9a4|p_ceilng.c:149]] (global)
- [[switch_DOOM_6cde57d1|p_ceilng.c:185]] (EV_DoCeiling)
- [[switch_DOOM_ffa690ec|p_plats.c:154]] (EV_DoPlat)

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
