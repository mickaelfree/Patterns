---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/fallthrough
date: 2025-04-25
pattern_type: switch
pattern_variant: fallthrough
source_file: d_main.c
line: 817
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Aiguillage multiple (SWITCH) (Fallthrough)

## Contexte
- **Fichier**: `d_main.c`
- **Ligne**: 817
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
      case retail:
	sprintf (title,
		 "                         "
		 "The Ultimate DOOM Startup v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
      case shareware:
	sprintf (title,
		 "                            "
		 "DOOM Shareware Startup v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
      case registered:
	sprintf (title,
		 "                            "
		 "DOOM Registered Startup v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
      case commercial:
	sprintf (title,
		 "                         "
		 "DOOM 2: Hell on Earth v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
/*FIXME
       case pack_plut:
	sprintf (title,
		 "                   "
		 "DOOM 2: Plutonia Experiment v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
      case pack_tnt:
	sprintf (title,
		 "                     "
		 "DOOM 2: TNT - Evilution v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
	break;
*/
      default:
	sprintf (title,
		 "                     "
		 "Public DOOM - v%i.%i"
		 "                           ",
		 VERSION/100,VERSION%100);
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
