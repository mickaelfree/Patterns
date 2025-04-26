---
tags: pattern, pattern/do-while, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: do while
pattern_variant: simple
source_file: r_draw.c
line: 435
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Tapis roulant à activation garantie (DO WHILE) (Tapis à activation unique)

## Contexte
- **Fichier**: `r_draw.c`
- **Ligne**: 435
- **Fonction**: R_DrawTranslatedColumn
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
	// Translation tables are used
	//  to map certain colorramps to other ones,
	//  used with PLAY sprites.
	// Thus the "green" ramp of the player 0 sprite
	//  is mapped to gray, red, black/indigo. 
	*dest = dc_colormap[dc_translation[dc_source[frac>>FRACBITS]]];
	dest += SCREENWIDTH;
	
	frac += fracstep; 
    } while (count--);
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant à activation garantie dans Factorio. Il comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.*

## Patterns Similaires
- [[do_while_DOOM_22867d1f|r_draw.c:138]] (R_DrawColumn)
- [[do_while_DOOM_aaa04fc0|r_draw.c:244]] (R_DrawColumnLow)
- [[do_while_DOOM_a360c0fa|r_draw.c:352]] (R_DrawFuzzColumn)
- [[do_while_DOOM_295c7e64|r_draw.c:549]] (R_DrawSpan)

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
