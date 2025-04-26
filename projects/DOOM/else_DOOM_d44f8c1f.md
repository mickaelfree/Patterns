---
tags: pattern, pattern/else, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else
pattern_variant: simple
source_file: hu_stuff.c
line: 547
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Répartiteur alternatif (ELSE) (Répartiteur simple)

## Contexte
- **Fichier**: `hu_stuff.c`
- **Ligne**: 547
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Répartiteur simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Répartiteur alternatif**

Comme un répartiteur qui dirige les ressources vers un chemin alternatif.

## Code Source
```c
else
		{
		    if (c >= 'a' && c <= 'z')
			c = (char) shiftxform[(unsigned char) c];
		    rc = HUlib_keyInIText(&w_inputbuffer[i], c);
		    if (rc && c == KEY_ENTER)
		    {
			if (w_inputbuffer[i].l.len
			    && (chat_dest[i] == consoleplayer+1
				|| chat_dest[i] == HU_BROADCAST))
			{
			    HUlib_addMessageToSText(&w_message,
						    player_names[i],
						    w_inputbuffer[i].l.l);
			    
			    message_nottobefuckedwith = true;
			    message_on = true;
			    message_counter = HU_MSGTIMEOUT;
			    if ( gamemode == commercial )
			      S_StartSound(0, sfx_radio);
			    else
			      S_StartSound(0, sfx_tink);
			}
			HUlib_resetIText(&w_inputbuffer[i]);
		    }
		}
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur alternatif dans Factorio. Il comme un répartiteur qui dirige les ressources vers un chemin alternatif.*

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
