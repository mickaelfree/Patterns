---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: switch
pattern_variant: simple
source_file: p_ceilng.c
line: 114
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔀 Aiguillage multiple (SWITCH) (Simple)

## Contexte
- **Fichier**: `p_ceilng.c`
- **Ligne**: 114
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch(ceiling->type)
	    {
	      case silentCrushAndRaise: break;
	      default:
		S_StartSound((mobj_t *)&ceiling->sector->soundorg,
			     sfx_stnmov);
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
- [[switch_DOOM_8f178fd2|p_ceilng.c:70]] (global)
- [[switch_DOOM_f0f39b22|p_ceilng.c:125]] (global)
- [[switch_DOOM_bd5ca9a4|p_ceilng.c:149]] (global)

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
