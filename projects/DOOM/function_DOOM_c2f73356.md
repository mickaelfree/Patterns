---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_ceilng.c
line: 291
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_ceilng.c`
- **Ligne**: 291
- **Fonction**: P_ActivateInStasisCeiling
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void P_ActivateInStasisCeiling(line_t* line)
{
    int		i;
	
    for (i = 0;i < MAXCEILINGS;i++)
    {
	if (activeceilings[i]
	    && (activeceilings[i]->tag == line->tag)
	    && (activeceilings[i]->direction == 0))
	{
	    activeceilings[i]->direction = activeceilings[i]->olddirection;
	    activeceilings[i]->thinker.function.acp1
	      = (actionf_p1)T_MoveCeiling;
	}
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_695b9a7e|p_ceilng.c:314]] (EV_CeilingCrushStop)
- [[function_DOOM_e044292a|p_ceilng.c:251]] (P_AddActiveCeiling)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_DOOM_3e1b4f0f|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
