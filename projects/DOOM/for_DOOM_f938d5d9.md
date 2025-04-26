---
tags: pattern, pattern/for, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: for
pattern_variant: simple
source_file: am_map.c
line: 1204
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Chaîne de montage (FOR) (Chaîne simple)

## Contexte
- **Fichier**: `am_map.c`
- **Ligne**: 1204
- **Fonction**: AM_drawLineCharacter
- **Projet**: DOOM
- **Variante**: Chaîne simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Chaîne de montage**

Comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.

## Code Source
```c
for (i=0;i<lineguylines;i++)
    {
	l.a.x = lineguy[i].a.x;
	l.a.y = lineguy[i].a.y;

	if (scale)
	{
	    l.a.x = FixedMul(scale, l.a.x);
	    l.a.y = FixedMul(scale, l.a.y);
	}

	if (angle)
	    AM_rotate(&l.a.x, &l.a.y, angle);

	l.a.x += x;
	l.a.y += y;

	l.b.x = lineguy[i].b.x;
	l.b.y = lineguy[i].b.y;

	if (scale)
	{
	    l.b.x = FixedMul(scale, l.b.x);
	    l.b.y = FixedMul(scale, l.b.y);
	}

	if (angle)
	    AM_rotate(&l.b.x, &l.b.y, angle);
	
	l.b.x += x;
	l.b.y += y;

	AM_drawMline(&l, color);
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
