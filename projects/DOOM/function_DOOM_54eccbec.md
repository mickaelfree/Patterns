---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: wi_stuff.c
line: 421
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `wi_stuff.c`
- **Ligne**: 421
- **Fonction**: WI_drawLF
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void WI_drawLF(void)
{
    int y = WI_TITLEY;

    // draw <LevelName> 
    V_DrawPatch((SCREENWIDTH - SHORT(lnames[wbs->last]->width))/2,
		y, FB, lnames[wbs->last]);

    // draw "Finished!"
    y += (5*SHORT(lnames[wbs->last]->height))/4;
    
    V_DrawPatch((SCREENWIDTH - SHORT(finished->width))/2,
		y, FB, finished);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_199a3844|wi_stuff.c:439]] (WI_drawEL)
- [[function_DOOM_01c1f085|g_game.c:445]] (G_DoLoadLevel)
- [[function_DOOM_440bc1e5|f_finale.c:207]] (F_Ticker)
- [[function_DOOM_cc624e29|p_tick.c:130]] (P_Ticker)
- [[function_DOOM_6337c920|st_stuff.c:1207]] (ST_loadData)

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
