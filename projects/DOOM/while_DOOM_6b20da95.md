---
tags: pattern, pattern/while, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: while
pattern_variant: simple
source_file: v_video.c
line: 313
project: DOOM
first_seen: 2025-04-25
occurrences: 3
ai_analyzed: non
optimizable: non
---

# ⭕ Tapis roulant surveillé (WHILE) (Tapis standard)

## Contexte
- **Fichier**: `v_video.c`
- **Ligne**: 313
- **Fonction**: while
- **Projet**: DOOM
- **Variante**: Tapis standard
- **Complexité**: standard

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (column->topdelta != 0xff ) 
	{ 
	    source = (byte *)column + 3; 
	    dest = desttop + column->topdelta*SCREENWIDTH; 
	    count = column->length; 
			 
	    while (count--) 
	    { 
		*dest = *source++; 
		dest += SCREENWIDTH; 
	    } 
	    column = (column_t *)(  (byte *)column + column->length 
				    + 4 ); 
	}
```

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_DOOM_c92a7f99|v_video.c:379]] (while)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 3 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[for_DOOM_b08db244|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_790f12f4|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_fe5c5de5|🔄 Chaîne de montage (FOR)]]
[[do_while_DOOM_f95c2f34|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_b1640881|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_cd442d3d|🔄 Tapis roulant à activation garantie (DO WHILE)]]
