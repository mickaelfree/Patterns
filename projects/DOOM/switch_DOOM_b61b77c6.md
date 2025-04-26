---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/fallthrough
date: 2025-04-25
pattern_type: switch
pattern_variant: fallthrough
source_file: p_doors.c
line: 419
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Aiguillage multiple (SWITCH) (Fallthrough)

## Contexte
- **Fichier**: `p_doors.c`
- **Ligne**: 419
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Fallthrough
- **Complexité**: avancée

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch(line->special)
	{
	  case	1: // ONLY FOR "RAISE" DOORS, NOT "OPEN"s
	  case	26:
	  case	27:
	  case	28:
	  case	117:
	    if (door->direction == -1)
		door->direction = 1;	// go back up
	    else
	    {
		if (!thing->player)
		    return;		// JDC: bad guys never close doors
		
		door->direction = -1;	// start going down immediately
	    }
	    return;
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

## Patterns Similaires
- [[switch_DOOM_d959a95d|p_switch.c:307]] (P_UseSpecialLine)
- [[switch_DOOM_ba1c01c9|p_doors.c:440]] (switch)
- [[switch_DOOM_4ff28abc|p_switch.c:286]] (P_UseSpecialLine)
- [[switch_DOOM_5825efc2|p_doors.c:219]] (EV_DoLockedDoor)
- [[switch_DOOM_657a236e|p_doors.c:369]] (global)

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
