---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: hu_lib.c
line: 99
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `hu_lib.c`
- **Ligne**: 99
- **Fonction**: HUlib_delCharFromTextLine
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
HUlib_drawTextLine
( hu_textline_t*	l,
  boolean		drawcursor )
{

    int			i;
    int			w;
    int			x;
    unsigned char	c;

    // draw the new stuff
    x = l->x;
    for (i=0;i<l->len;i++)
    {
	c = toupper(l->l[i]);
	if (c != ' '
	    && c >= l->sc
	    && c <= '_')
	{
	    w = SHORT(l->f[c - l->sc]->width);
	    if (x+w > SCREENWIDTH)
		break;
	    V_DrawPatchDirect(x, l->y, FG, l->f[c - l->sc]);
	    x += w;
	}
	else
	{
	    x += 4;
	    if (x >= SCREENWIDTH)
		break;
	}
    }

    // draw the cursor if requested
    if (drawcursor
	&& x + SHORT(l->f['_' - l->sc]->width) <= SCREENWIDTH)
    {
	V_DrawPatchDirect(x, l->y, FG, l->f['_' - l->sc]);
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_5b0b7660|hu_lib.c:46]] (HUlib_init)
- [[function_DOOM_2fc270e8|r_main.c:544]] (R_InitTextureMapping)
- [[function_DOOM_fa329fc8|hu_lib.c:200]] (HUlib_initSText)
- [[function_DOOM_a733c8e2|am_map.c:1055]] (AM_drawMline)

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
