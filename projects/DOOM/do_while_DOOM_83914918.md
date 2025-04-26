---
tags: pattern, pattern/do-while, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: do while
pattern_variant: simple
source_file: r_draw.c
line: 674
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Tapis roulant à activation garantie (DO WHILE) (Tapis à activation unique)

## Contexte
- **Fichier**: `r_draw.c`
- **Ligne**: 674
- **Fonction**: R_DrawSpanLow
- **Projet**: DOOM
- **Variante**: Tapis à activation unique
- **Complexité**: standard

## Métaphore Factorio
🔄 **Tapis roulant à activation garantie**

Comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.

## Code Source
```c
do 
    { 
	spot = ((yfrac>>(16-6))&(63*64)) + ((xfrac>>16)&63);
	// Lowres/blocky mode does it twice,
	//  while scale is adjusted appropriately.
	*dest++ = ds_colormap[ds_source[spot]]; 
	*dest++ = ds_colormap[ds_source[spot]];
	
	xfrac += ds_xstep; 
	yfrac += ds_ystep; 

    } while (count--);
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant à activation garantie dans Factorio. Il comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.*

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
[[for_DOOM_b08db244|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_790f12f4|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_fe5c5de5|🔄 Chaîne de montage (FOR)]]
