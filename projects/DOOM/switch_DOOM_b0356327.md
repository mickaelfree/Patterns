---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/fallthrough
date: 2025-04-25
pattern_type: switch
pattern_variant: fallthrough
source_file: d_main.c
line: 1065
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Aiguillage multiple (SWITCH) (Fallthrough)

## Contexte
- **Fichier**: `d_main.c`
- **Ligne**: 1065
- **Fonction**: D_DoomMain
- **Projet**: DOOM
- **Variante**: Fallthrough
- **Complexité**: avancée

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch ( gamemode )
    {
      case shareware:
      case indetermined:
	printf (
	    "===========================================================================\n"
	    "                                Shareware!\n"
	    "===========================================================================\n"
	);
	break;
      case registered:
      case retail:
      case commercial:
	printf (
	    "===========================================================================\n"
	    "                 Commercial product - do not distribute!\n"
	    "         Please report software piracy to the SPA: 1-800-388-PIR8\n"
	    "===========================================================================\n"
	);
	break;
	
      default:
	// Ouch.
	break;
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

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
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
