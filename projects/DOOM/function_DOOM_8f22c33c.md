---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: wi_stuff.c
line: 583
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `wi_stuff.c`
- **Ligne**: 583
- **Fonction**: WI_drawAnimatedBack
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void WI_drawAnimatedBack(void)
{
    int			i;
    anim_t*		a;

    if (commercial)
	return;

    if (wbs->epsd > 2)
	return;

    for (i=0 ; i<NUMANIMS[wbs->epsd] ; i++)
    {
	a = &anims[wbs->epsd][i];

	if (a->ctr >= 0)
	    V_DrawPatch(a->loc.x, a->loc.y, FB, a->p[a->ctr]);
    }

}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_2b2b7ede|wi_stuff.c:503]] (WI_drawOnLnode)

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
