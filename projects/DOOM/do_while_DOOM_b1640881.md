---
tags: pattern, pattern/do-while, factorio, code-logic, project/DOOM, pattern/variant/potential_infinite
date: 2025-04-25
pattern_type: do while
pattern_variant: potential_infinite
source_file: d_main.c
line: 767
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔄 Tapis roulant à activation garantie (DO WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `d_main.c`
- **Ligne**: 767
- **Fonction**: FindResponseFile
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
		myargv[indexinfile++] = infile+k;
		while(k < size &&
		      ((*(infile+k)>= ' '+1) && (*(infile+k)<='z')))
		    k++;
		*(infile+k) = 0;
		while(k < size &&
		      ((*(infile+k)<= ' ') || (*(infile+k)>'z')))
		    k++;
	    } while(k < size);
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
