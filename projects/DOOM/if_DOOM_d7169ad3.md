---
tags: pattern, pattern/if, factorio, code-logic, project/DOOM, pattern/variant/complex
date: 2025-04-25
pattern_type: if
pattern_variant: complex
source_file: d_net.c
line: 686
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Réseau de capteurs)

## Contexte
- **Fichier**: `d_net.c`
- **Ligne**: 686
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Réseau de capteurs
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (!demoplayback)
    {	
	// ideally nettics[0] should be 1 - 3 tics above lowtic
	// if we are consistantly slower, speed up time
	for (i=0 ; i<MAXPLAYERS ; i++)
	    if (playeringame[i])
		break;
	if (consoleplayer == i)
	{
	    // the key player does not adapt
	}
	else
	{
	    if (nettics[0] <= nettics[nodeforplayer[i]])
	    {
		gametime--;
		// printf ("-");
	    }
	    frameskip[frameon&3] = (oldnettics > nettics[nodeforplayer[i]]);
	    oldnettics = nettics[0];
	    if (frameskip[0] && frameskip[1] && frameskip[2] && frameskip[3])
	    {
		skiptics = 1;
		// printf ("+");
	    }
	}
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
- [[if_DOOM_4d1cb5d5|p_inter.c:835]] (if)
- [[if_DOOM_473ea493|r_segs.c:456]] (global)
- [[if_DOOM_11f5fbb9|p_pspr.c:406]] (A_Lower)
- [[if_DOOM_df3a8fff|hu_stuff.c:735]] (global)
- [[if_DOOM_9f401027|p_enemy.c:295]] (P_Move)

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
