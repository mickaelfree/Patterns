---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_doors.c
line: 566
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_doors.c`
- **Ligne**: 566
- **Fonction**: P_InitSlidingDoorFrames
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void P_InitSlidingDoorFrames(void)
{
    int		i;
    int		f1;
    int		f2;
    int		f3;
    int		f4;
	
    // DOOM II ONLY...
    if ( gamemode != commercial)
	return;
	
    for (i = 0;i < MAXSLIDEDOORS; i++)
    {
	if (!slideFrameNames[i].frontFrame1[0])
	    break;
			
	f1 = R_TextureNumForName(slideFrameNames[i].frontFrame1);
	f2 = R_TextureNumForName(slideFrameNames[i].frontFrame2);
	f3 = R_TextureNumForName(slideFrameNames[i].frontFrame3);
	f4 = R_TextureNumForName(slideFrameNames[i].frontFrame4);

	slideFrames[i].frontFrames[0] = f1;
	slideFrames[i].frontFrames[1] = f2;
	slideFrames[i].frontFrames[2] = f3;
	slideFrames[i].frontFrames[3] = f4;
		
	f1 = R_TextureNumForName(slideFrameNames[i].backFrame1);
	f2 = R_TextureNumForName(slideFrameNames[i].backFrame2);
	f3 = R_TextureNumForName(slideFrameNames[i].backFrame3);
	f4 = R_TextureNumForName(slideFrameNames[i].backFrame4);

	slideFrames[i].backFrames[0] = f1;
	slideFrames[i].backFrames[1] = f2;
	slideFrames[i].backFrames[2] = f3;
	slideFrames[i].backFrames[3] = f4;
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_c32b2fdf|r_main.c:612]] (R_InitLightTables)
- [[function_DOOM_51d7dfcd|i_video.c:692]] (I_InitGraphics)
- [[function_DOOM_2fc270e8|r_main.c:544]] (R_InitTextureMapping)
- [[function_DOOM_f1ae68d5|st_stuff.c:1124]] (ST_Drawer)
- [[function_DOOM_1ce10c7b|d_net.c:368]] (NetUpdate)

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
