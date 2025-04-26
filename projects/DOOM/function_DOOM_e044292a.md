---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_ceilng.c
line: 251
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_ceilng.c`
- **Ligne**: 251
- **Fonction**: P_AddActiveCeiling
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void P_AddActiveCeiling(ceiling_t* c)
{
    int		i;
    
    for (i = 0; i < MAXCEILINGS;i++)
    {
	if (activeceilings[i] == NULL)
	{
	    activeceilings[i] = c;
	    return;
	}
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_ec01a880|p_plats.c:288]] (EV_StopPlat)
- [[function_DOOM_8c6a5174|p_ceilng.c:270]] (P_RemoveActiveCeiling)
- [[function_DOOM_47597e68|d_net.c:555]] (D_CheckNetGame)
- [[function_DOOM_0099153b|p_spec.c:433]] (P_FindSectorFromLineTag)

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
