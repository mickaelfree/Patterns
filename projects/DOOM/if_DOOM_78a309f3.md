---
tags: pattern, pattern/if, factorio, code-logic, project/DOOM, pattern/variant/complex
date: 2025-04-25
pattern_type: if
pattern_variant: complex
source_file: am_map.c
line: 1311
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Réseau de capteurs)

## Contexte
- **Fichier**: `am_map.c`
- **Ligne**: 1311
- **Fonction**: AM_drawMarks
- **Projet**: DOOM
- **Variante**: Réseau de capteurs
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (markpoints[i].x != -1)
	{
	    //      w = SHORT(marknums[i]->width);
	    //      h = SHORT(marknums[i]->height);
	    w = 5; // because something's wrong with the wad, i guess
	    h = 6; // because something's wrong with the wad, i guess
	    fx = CXMTOF(markpoints[i].x);
	    fy = CYMTOF(markpoints[i].y);
	    if (fx >= f_x && fx <= f_w - w && fy >= f_y && fy <= f_h - h)
		V_DrawPatch(fx, fy, FB, marknums[i]);
	}
```

## Analyse Structurelle
**Type détecté**: Réseau de capteurs

Ce réseau complexe de conditions pourrait être simplifié ou décomposé en sous-fonctions plus lisibles.

**Analogie Factorio**:
Comme un réseau de circuits logiques complexe qui pourrait être remplacé par un circuit combinatoire plus simple.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_DOOM_152def17|r_data.c:359]] (global)
- [[if_DOOM_ad63a29a|wi_stuff.c:1508]] (WI_Ticker)
- [[if_DOOM_143ab716|st_stuff.c:761]] (global)
- [[if_DOOM_6a34b790|p_maputl.c:305]] (P_LineOpening)
- [[if_DOOM_fbd295c0|w_wad.c:447]] (W_ReadLump)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_DOOM_15ea13cc|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_0faf1aab|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_29abfc46|🔀 Répartiteur alternatif (ELSE)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
[[switch_DOOM_83fe174e|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_17419957|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_b47d2988|🔀 Aiguillage multiple (SWITCH)]]
