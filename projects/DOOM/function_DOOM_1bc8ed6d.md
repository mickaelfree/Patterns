---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: v_video.c
line: 482
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `v_video.c`
- **Ligne**: 482
- **Fonction**: V_Init
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void V_Init (void) 
{ 
    int		i;
    byte*	base;
		
    // stick these in low dos memory on PCs

    base = I_AllocLow (SCREENWIDTH*SCREENHEIGHT*4);

    for (i=0 ; i<4 ; i++)
	screens[i] = base + i*SCREENWIDTH*SCREENHEIGHT;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_c34377e0|i_video.c:930]] (InitExpand2)
- [[function_DOOM_8e537385|p_spec.c:148]] (P_InitPicAnims)
- [[function_DOOM_440bc1e5|f_finale.c:207]] (F_Ticker)
- [[function_DOOM_cc624e29|p_tick.c:130]] (P_Ticker)
- [[function_DOOM_953c4d5c|m_misc.c:503]] (M_ScreenShot)

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
