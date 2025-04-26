---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: f_finale.c
line: 700
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `f_finale.c`
- **Ligne**: 700
- **Fonction**: F_Drawer
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void F_Drawer (void)
{
    if (finalestage == 2)
    {
	F_CastDrawer ();
	return;
    }

    if (!finalestage)
	F_TextWrite ();
    else
    {
	switch (gameepisode)
	{
	  case 1:
	    if ( gamemode == retail )
	      V_DrawPatch (0,0,0,
			 W_CacheLumpName("CREDIT",PU_CACHE));
	    else
	      V_DrawPatch (0,0,0,
			 W_CacheLumpName("HELP2",PU_CACHE));
	    break;
	  case 2:
	    V_DrawPatch(0,0,0,
			W_CacheLumpName("VICTORY2",PU_CACHE));
	    break;
	  case 3:
	    F_BunnyScroll ();
	    break;
	  case 4:
	    V_DrawPatch (0,0,0,
			 W_CacheLumpName("ENDPIC",PU_CACHE));
	    break;
	}
    }
			
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
