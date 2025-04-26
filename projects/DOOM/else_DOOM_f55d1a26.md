---
tags: pattern, pattern/else, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else
pattern_variant: simple
source_file: r_segs.c
line: 291
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Répartiteur alternatif (ELSE) (Répartiteur simple)

## Contexte
- **Fichier**: `r_segs.c`
- **Ligne**: 291
- **Fonction**: if
- **Projet**: DOOM
- **Variante**: Répartiteur simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Répartiteur alternatif**

Comme un répartiteur qui dirige les ressources vers un chemin alternatif.

## Code Source
```c
else
	{
	    // two sided line
	    if (toptexture)
	    {
		// top wall
		mid = pixhigh>>HEIGHTBITS;
		pixhigh += pixhighstep;

		if (mid >= floorclip[rw_x])
		    mid = floorclip[rw_x]-1;

		if (mid >= yl)
		{
		    dc_yl = yl;
		    dc_yh = mid;
		    dc_texturemid = rw_toptexturemid;
		    dc_source = R_GetColumn(toptexture,texturecolumn);
		    colfunc ();
		    ceilingclip[rw_x] = mid;
		}
		else
		    ceilingclip[rw_x] = yl-1;
	    }
	    else
	    {
		// no top wall
		if (markceiling)
		    ceilingclip[rw_x] = yl-1;
	    }
			
	    if (bottomtexture)
	    {
		// bottom wall
		mid = (pixlow+HEIGHTUNIT-1)>>HEIGHTBITS;
		pixlow += pixlowstep;

		// no space above wall?
		if (mid <= ceilingclip[rw_x])
		    mid = ceilingclip[rw_x]+1;
		
		if (mid <= yh)
		{
		    dc_yl = mid;
		    dc_yh = yh;
		    dc_texturemid = rw_bottomtexturemid;
		    dc_source = R_GetColumn(bottomtexture,
					    texturecolumn);
		    colfunc ();
		    floorclip[rw_x] = mid;
		}
		else
		    floorclip[rw_x] = yh+1;
	    }
	    else
	    {
		// no bottom wall
		if (markfloor)
		    floorclip[rw_x] = yh+1;
	    }
			
	    if (maskedtexture)
	    {
		// save texturecol
		//  for backdrawing of masked mid texture
		maskedtexturecol[rw_x] = texturecolumn;
	    }
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur alternatif dans Factorio. Il comme un répartiteur qui dirige les ressources vers un chemin alternatif.*

## Patterns Similaires
- [[else_DOOM_7ae5dbc4|d_net.c:507]] (global)
- [[else_DOOM_fe2f050f|f_finale.c:415]] (F_CastTicker)
- [[else_DOOM_3d23fea9|g_game.c:933]] (global)
- [[else_DOOM_1b8a24c7|i_sound.c:807]] (I_InitSound)
- [[else_DOOM_abd594b5|i_video.c:504]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
