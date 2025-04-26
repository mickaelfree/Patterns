---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_switch.c
line: 275
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_switch.c`
- **Ligne**: 275
- **Fonction**: P_UseSpecialLine
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
boolean
P_UseSpecialLine
( mobj_t*	thing,
  line_t*	line,
  int		side )
{               

    // Err...
    // Use the back sides of VERY SPECIAL lines...
    if (side)
    {
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
    }

    
    // Switches that other things can activate.
    if (!thing->player)
    {
	// never open secret doors
	if (line->flags & ML_SECRET)
	    return false;
	
	switch(line->special)
	{
	  case 1: 	// MANUAL DOOR RAISE
	  case 32:	// MANUAL BLUE
	  case 33:	// MANUAL RED
	  case 34:	// MANUAL YELLOW
	    break;
	    
	  default:
	    return false;
	    break;
	}
    }

    
    // do something  
    switch (line->special)
    {
	// MANUALS
      case 1:		// Vertical Door
      case 26:		// Blue Door/Locked
      case 27:		// Yellow Door /Locked
      case 28:		// Red Door /Locked

      case 31:		// Manual door open
      case 32:		// Blue locked door open
      case 33:		// Red locked door open
      case 34:		// Yellow locked door open

      case 117:		// Blazing door raise
      case 118:		// Blazing door open
	EV_VerticalDoor (line, thing);
	break;
	
	//UNUSED - Door Slide Open&Close
	// case 124:
	// EV_SlidingDoor (line, thing);
	// break;

	// SWITCHES
      case 7:
	// Build Stairs
	if (EV_BuildStairs(line,build8))
	    P_ChangeSwitchTexture(line,0);
	break;

      case 9:
	// Change Donut
	if (EV_DoDonut(line))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 11:
	// Exit level
	P_ChangeSwitchTexture(line,0);
	G_ExitLevel ();
	break;
	
      case 14:
	// Raise Floor 32 and change texture
	if (EV_DoPlat(line,raiseAndChange,32))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 15:
	// Raise Floor 24 and change texture
	if (EV_DoPlat(line,raiseAndChange,24))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 18:
	// Raise Floor to next highest floor
	if (EV_DoFloor(line, raiseFloorToNearest))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 20:
	// Raise Plat next highest floor and change texture
	if (EV_DoPlat(line,raiseToNearestAndChange,0))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 21:
	// PlatDownWaitUpStay
	if (EV_DoPlat(line,downWaitUpStay,0))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 23:
	// Lower Floor to Lowest
	if (EV_DoFloor(line,lowerFloorToLowest))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 29:
	// Raise Door
	if (EV_DoDoor(line,normal))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 41:
	// Lower Ceiling to Floor
	if (EV_DoCeiling(line,lowerToFloor))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 71:
	// Turbo Lower Floor
	if (EV_DoFloor(line,turboLower))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 49:
	// Ceiling Crush And Raise
	if (EV_DoCeiling(line,crushAndRaise))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 50:
	// Close Door
	if (EV_DoDoor(line,close))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 51:
	// Secret EXIT
	P_ChangeSwitchTexture(line,0);
	G_SecretExitLevel ();
	break;
	
      case 55:
	// Raise Floor Crush
	if (EV_DoFloor(line,raiseFloorCrush))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 101:
	// Raise Floor
	if (EV_DoFloor(line,raiseFloor))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 102:
	// Lower Floor to Surrounding floor height
	if (EV_DoFloor(line,lowerFloor))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 103:
	// Open Door
	if (EV_DoDoor(line,open))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 111:
	// Blazing Door Raise (faster than TURBO!)
	if (EV_DoDoor (line,blazeRaise))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 112:
	// Blazing Door Open (faster than TURBO!)
	if (EV_DoDoor (line,blazeOpen))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 113:
	// Blazing Door Close (faster than TURBO!)
	if (EV_DoDoor (line,blazeClose))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 122:
	// Blazing PlatDownWaitUpStay
	if (EV_DoPlat(line,blazeDWUS,0))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 127:
	// Build Stairs Turbo 16
	if (EV_BuildStairs(line,turbo16))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 131:
	// Raise Floor Turbo
	if (EV_DoFloor(line,raiseFloorTurbo))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 133:
	// BlzOpenDoor BLUE
      case 135:
	// BlzOpenDoor RED
      case 137:
	// BlzOpenDoor YELLOW
	if (EV_DoLockedDoor (line,blazeOpen,thing))
	    P_ChangeSwitchTexture(line,0);
	break;
	
      case 140:
	// Raise Floor 512
	if (EV_DoFloor(line,raiseFloor512))
	    P_ChangeSwitchTexture(line,0);
	break;
	
	// BUTTONS
      case 42:
	// Close Door
	if (EV_DoDoor(line,close))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 43:
	// Lower Ceiling to Floor
	if (EV_DoCeiling(line,lowerToFloor))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 45:
	// Lower Floor to Surrounding floor height
	if (EV_DoFloor(line,lowerFloor))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 60:
	// Lower Floor to Lowest
	if (EV_DoFloor(line,lowerFloorToLowest))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 61:
	// Open Door
	if (EV_DoDoor(line,open))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 62:
	// PlatDownWaitUpStay
	if (EV_DoPlat(line,downWaitUpStay,1))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 63:
	// Raise Door
	if (EV_DoDoor(line,normal))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 64:
	// Raise Floor to ceiling
	if (EV_DoFloor(line,raiseFloor))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 66:
	// Raise Floor 24 and change texture
	if (EV_DoPlat(line,raiseAndChange,24))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 67:
	// Raise Floor 32 and change texture
	if (EV_DoPlat(line,raiseAndChange,32))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 65:
	// Raise Floor Crush
	if (EV_DoFloor(line,raiseFloorCrush))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 68:
	// Raise Plat to next highest floor and change texture
	if (EV_DoPlat(line,raiseToNearestAndChange,0))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 69:
	// Raise Floor to next highest floor
	if (EV_DoFloor(line, raiseFloorToNearest))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 70:
	// Turbo Lower Floor
	if (EV_DoFloor(line,turboLower))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 114:
	// Blazing Door Raise (faster than TURBO!)
	if (EV_DoDoor (line,blazeRaise))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 115:
	// Blazing Door Open (faster than TURBO!)
	if (EV_DoDoor (line,blazeOpen))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 116:
	// Blazing Door Close (faster than TURBO!)
	if (EV_DoDoor (line,blazeClose))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 123:
	// Blazing PlatDownWaitUpStay
	if (EV_DoPlat(line,blazeDWUS,0))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 132:
	// Raise Floor Turbo
	if (EV_DoFloor(line,raiseFloorTurbo))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 99:
	// BlzOpenDoor BLUE
      case 134:
	// BlzOpenDoor RED
      case 136:
	// BlzOpenDoor YELLOW
	if (EV_DoLockedDoor (line,blazeOpen,thing))
	    P_ChangeSwitchTexture(line,1);
	break;
	
      case 138:
	// Light Turn On
	EV_LightTurnOn(line,255);
	P_ChangeSwitchTexture(line,1);
	break;
	
      case 139:
	// Light Turn Off
	EV_LightTurnOn(line,35);
	P_ChangeSwitchTexture(line,1);
	break;
			
    }
	
    return true;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_9c4a0871|p_spec.c:958]] (P_ShootSpecialLine)
- [[function_DOOM_e66d2d08|p_spec.c:491]] (P_CrossSpecialLine)
- [[function_DOOM_59436a72|p_map.c:1257]] (PIT_ChangeSector)

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
