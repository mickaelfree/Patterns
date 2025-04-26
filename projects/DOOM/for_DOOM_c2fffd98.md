---
tags: pattern, pattern/for, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: for
pattern_variant: simple
source_file: p_sight.c
line: 166
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Chaîne de montage (FOR) (Chaîne simple)

## Contexte
- **Fichier**: `p_sight.c`
- **Ligne**: 166
- **Fonction**: P_CrossSubsector
- **Projet**: DOOM
- **Variante**: Chaîne simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Chaîne de montage**

Comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.

## Code Source
```c
for ( ; count ; seg++, count--)
    {
	line = seg->linedef;

	// allready checked other side?
	if (line->validcount == validcount)
	    continue;
	
	line->validcount = validcount;
		
	v1 = line->v1;
	v2 = line->v2;
	s1 = P_DivlineSide (v1->x,v1->y, &strace);
	s2 = P_DivlineSide (v2->x, v2->y, &strace);

	// line isn't crossed?
	if (s1 == s2)
	    continue;
	
	divl.x = v1->x;
	divl.y = v1->y;
	divl.dx = v2->x - v1->x;
	divl.dy = v2->y - v1->y;
	s1 = P_DivlineSide (strace.x, strace.y, &divl);
	s2 = P_DivlineSide (t2x, t2y, &divl);

	// line isn't crossed?
	if (s1 == s2)
	    continue;	

	// stop because it is not two sided anyway
	// might do this after updating validcount?
	if ( !(line->flags & ML_TWOSIDED) )
	    return false;
	
	// crosses a two sided line
	front = seg->frontsector;
	back = seg->backsector;

	// no wall to block sight with?
	if (front->floorheight == back->floorheight
	    && front->ceilingheight == back->ceilingheight)
	    continue;	

	// possible occluder
	// because of ceiling height differences
	if (front->ceilingheight < back->ceilingheight)
	    opentop = front->ceilingheight;
	else
	    opentop = back->ceilingheight;

	// because of ceiling height differences
	if (front->floorheight > back->floorheight)
	    openbottom = front->floorheight;
	else
	    openbottom = back->floorheight;
		
	// quick test for totally closed doors
	if (openbottom >= opentop)	
	    return false;		// stop
	
	frac = P_InterceptVector2 (&strace, &divl);
		
	if (front->floorheight != back->floorheight)
	{
	    slope = FixedDiv (openbottom - sightzstart , frac);
	    if (slope > bottomslope)
		bottomslope = slope;
	}
		
	if (front->ceilingheight != back->ceilingheight)
	{
	    slope = FixedDiv (opentop - sightzstart , frac);
	    if (slope < topslope)
		topslope = slope;
	}
		
	if (topslope <= bottomslope)
	    return false;		// stop				
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme chaîne de montage dans Factorio. Il comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.*

## Patterns Similaires
- [[for_DOOM_022fad03|p_setup.c:313]] (global)

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
