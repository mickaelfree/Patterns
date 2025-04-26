---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_doors.c
line: 712
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_doors.c`
- **Ligne**: 712
- **Fonction**: EV_SlidingDoor
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
EV_SlidingDoor
( line_t*	line,
  mobj_t*	thing )
{
    sector_t*		sec;
    slidedoor_t*	door;
	
    // DOOM II ONLY...
    if (gamemode != commercial)
	return;
    
    // Make sure door isn't already being animated
    sec = line->frontsector;
    door = NULL;
    if (sec->specialdata)
    {
	if (!thing->player)
	    return;
			
	door = sec->specialdata;
	if (door->type == sdt_openAndClose)
	{
	    if (door->status == sd_waiting)
		door->status = sd_closing;
	}
	else
	    return;
    }
    
    // Init sliding door vars
    if (!door)
    {
	door = Z_Malloc (sizeof(*door), PU_LEVSPEC, 0);
	P_AddThinker (&door->thinker);
	sec->specialdata = door;
		
	door->type = sdt_openAndClose;
	door->status = sd_opening;
	door->whichDoorIndex = P_FindSlidingDoorType(line);

	if (door->whichDoorIndex < 0)
	    I_Error("EV_SlidingDoor: Can't use texture for sliding door!");
			
	door->frontsector = sec;
	door->backsector = line->backsector;
	door->thinker.function = T_SlidingDoor;
	door->timer = SWAITTICS;
	door->frame = 0;
	door->line = line;
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_3e92983a|p_maputl.c:395]] (P_SetThingPosition)
- [[function_DOOM_e61c21d3|p_ceilng.c:171]] (EV_DoCeiling)
- [[function_DOOM_e66d2d08|p_spec.c:491]] (P_CrossSpecialLine)
- [[function_DOOM_897e24b0|p_plats.c:138]] (EV_DoPlat)
- [[function_DOOM_4d180fa0|p_maputl.c:300]] (P_LineOpening)

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
