---
tags: pattern, pattern/do-while, factorio, code-logic, project/DOOM, pattern/variant/potential_infinite
date: 2025-04-25
pattern_type: do while
pattern_variant: potential_infinite
source_file: wi_stuff.c
line: 469
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔄 Tapis roulant à activation garantie (DO WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `wi_stuff.c`
- **Ligne**: 469
- **Fonction**: WI_drawOnLnode
- **Projet**: DOOM
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
🔄 **Tapis roulant à activation garantie**

Comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.

## Code Source
```c
do
    {
	left = lnodes[wbs->epsd][n].x - SHORT(c[i]->leftoffset);
	top = lnodes[wbs->epsd][n].y - SHORT(c[i]->topoffset);
	right = left + SHORT(c[i]->width);
	bottom = top + SHORT(c[i]->height);

	if (left >= 0
	    && right < SCREENWIDTH
	    && top >= 0
	    && bottom < SCREENHEIGHT)
	{
	    fits = true;
	}
	else
	{
	    i++;
	}
    } while (!fits && i!=2);
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui s'active au moins une fois avant de risquer de tourner indéfiniment.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant à activation garantie dans Factorio. Il comme un tapis roulant qui s'active au moins une fois, puis continue selon une condition.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[while_DOOM_669fd485|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_589dde27|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_135bd103|⭕ Tapis roulant surveillé (WHILE)]]
[[for_DOOM_b08db244|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_790f12f4|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_fe5c5de5|🔄 Chaîne de montage (FOR)]]
