---
tags: pattern, pattern/for, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: for
pattern_variant: simple
source_file: p_enemy.c
line: 515
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Chaîne de montage (FOR) (Chaîne simple)

## Contexte
- **Fichier**: `p_enemy.c`
- **Ligne**: 515
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Chaîne simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Chaîne de montage**

Comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.

## Code Source
```c
for ( ; ; actor->lastlook = (actor->lastlook+1)&3 )
    {
	if (!playeringame[actor->lastlook])
	    continue;
			
	if (c++ == 2
	    || actor->lastlook == stop)
	{
	    // done looking
	    return false;	
	}
	
	player = &players[actor->lastlook];

	if (player->health <= 0)
	    continue;		// dead

	if (!P_CheckSight (actor, player->mo))
	    continue;		// out of sight
			
	if (!allaround)
	{
	    an = R_PointToAngle2 (actor->x,
				  actor->y, 
				  player->mo->x,
				  player->mo->y)
		- actor->angle;
	    
	    if (an > ANG90 && an < ANG270)
	    {
		dist = P_AproxDistance (player->mo->x - actor->x,
					player->mo->y - actor->y);
		// if real close, react anyway
		if (dist > MELEERANGE)
		    continue;	// behind back
	    }
	}
		
	actor->target = player->mo;
	return true;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme chaîne de montage dans Factorio. Il comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.*

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
[[do_while_DOOM_f95c2f34|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_b1640881|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_cd442d3d|🔄 Tapis roulant à activation garantie (DO WHILE)]]
