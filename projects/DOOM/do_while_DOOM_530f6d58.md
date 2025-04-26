---
tags: pattern, pattern/do-while, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: do while
pattern_variant: simple
source_file: p_pspr.c
line: 69
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Tapis roulant à activation garantie (DO WHILE) (Tapis à activation unique)

## Contexte
- **Fichier**: `p_pspr.c`
- **Ligne**: 69
- **Fonction**: P_SetPsprite
- **Projet**: DOOM
- **Variante**: Tapis à activation unique
- **Complexité**: standard

## Métaphore Factorio
🔄 **Tapis roulant à activation garantie**

Comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.

## Code Source
```c
do
    {
	if (!stnum)
	{
	    // object removed itself
	    psp->state = NULL;
	    break;	
	}
	
	state = &states[stnum];
	psp->state = state;
	psp->tics = state->tics;	// could be 0

	if (state->misc1)
	{
	    // coordinate set
	    psp->sx = state->misc1 << FRACBITS;
	    psp->sy = state->misc2 << FRACBITS;
	}
	
	// Call action routine.
	// Modified handling.
	if (state->action.acp2)
	{
	    state->action.acp2(player, psp);
	    if (!psp->state)
		break;
	}
	
	stnum = psp->state->nextstate;
	
    } while (!psp->tics);
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant à activation garantie dans Factorio. Il comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.*

## Patterns Similaires
- [[do_while_DOOM_b78c6761|z_zone.c:215]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[while_DOOM_669fd485|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_589dde27|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_135bd103|⭕ Tapis roulant surveillé (WHILE)]]
[[for_DOOM_b08db244|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_790f12f4|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_fe5c5de5|🔄 Chaîne de montage (FOR)]]
