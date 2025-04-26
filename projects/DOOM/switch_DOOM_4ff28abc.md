---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: switch
pattern_variant: simple
source_file: p_switch.c
line: 286
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔀 Aiguillage multiple (SWITCH) (Simple)

## Contexte
- **Fichier**: `p_switch.c`
- **Ligne**: 286
- **Fonction**: P_UseSpecialLine
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch(line->special)
	{
	  case 124:
	    // Sliding door open&close
	    // UNUSED?
	    break;

	  default:
	    return false;
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
- [[switch_DOOM_e23d2ed6|p_spec.c:980]] (P_ShootSpecialLine)
- [[switch_DOOM_b61b77c6|p_doors.c:419]] (global)
- [[switch_DOOM_d959a95d|p_switch.c:307]] (P_UseSpecialLine)
- [[switch_DOOM_657a236e|p_doors.c:369]] (global)
- [[switch_DOOM_e361038b|p_spec.c:969]] (P_ShootSpecialLine)

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
