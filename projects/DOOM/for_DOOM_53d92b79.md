---
tags: pattern, pattern/for, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: for
pattern_variant: simple
source_file: wi_stuff.c
line: 1292
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Chaîne de montage (FOR) (Chaîne simple)

## Contexte
- **Fichier**: `wi_stuff.c`
- **Ligne**: 1292
- **Fonction**: WI_drawNetgameStats
- **Projet**: DOOM
- **Variante**: Chaîne simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Chaîne de montage**

Comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.

## Code Source
```c
for (i=0 ; i<MAXPLAYERS ; i++)
    {
	if (!playeringame[i])
	    continue;

	x = NG_STATSX;
	V_DrawPatch(x-SHORT(p[i]->width), y, FB, p[i]);

	if (i == me)
	    V_DrawPatch(x-SHORT(p[i]->width), y, FB, star);

	x += NG_SPACINGX;
	WI_drawPercent(x-pwidth, y+10, cnt_kills[i]);	x += NG_SPACINGX;
	WI_drawPercent(x-pwidth, y+10, cnt_items[i]);	x += NG_SPACINGX;
	WI_drawPercent(x-pwidth, y+10, cnt_secret[i]);	x += NG_SPACINGX;

	if (dofrags)
	    WI_drawNum(x, y+10, cnt_frags[i], -1);

	y += WI_SPACINGY;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme chaîne de montage dans Factorio. Il comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.*

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
