---
tags: pattern, pattern/else-if, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else if
pattern_variant: simple
source_file: am_map.c
line: 1147
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Répartiteur intelligent (ELSE IF) (Filtrage simple)

## Contexte
- **Fichier**: `am_map.c`
- **Ligne**: 1147
- **Fonction**: if
- **Projet**: DOOM
- **Variante**: Filtrage simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Répartiteur intelligent**

Comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.

## Code Source
```c
else if (lines[i].backsector->floorheight
			   != lines[i].frontsector->floorheight) {
		    AM_drawMline(&l, FDWALLCOLORS + lightlev); // floor level change
		}
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur intelligent dans Factorio. Il comme un répartiteur filtrant qui dirige les ressources vers différentes sorties selon des conditions.*

## Patterns Similaires
- [[else_if_DOOM_a7eb9f4d|am_map.c:1151]] (if)
- [[else_if_DOOM_6b3b9ca8|am_map.c:1155]] (if)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_DOOM_15ea13cc|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_0faf1aab|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_29abfc46|🔀 Répartiteur alternatif (ELSE)]]
[[switch_DOOM_83fe174e|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_17419957|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_b47d2988|🔀 Aiguillage multiple (SWITCH)]]
