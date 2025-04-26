---
tags: pattern, pattern/else, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: else
pattern_variant: simple
source_file: d_net.c
line: 507
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔀 Répartiteur alternatif (ELSE) (Répartiteur simple)

## Contexte
- **Fichier**: `d_net.c`
- **Ligne**: 507
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
	// key player, send the setup info
	printf ("sending network start info...\n");
	do
	{
	    CheckAbort ();
	    for (i=0 ; i<doomcom->numnodes ; i++)
	    {
		netbuffer->retransmitfrom = startskill;
		if (deathmatch)
		    netbuffer->retransmitfrom |= (deathmatch<<6);
		if (nomonsters)
		    netbuffer->retransmitfrom |= 0x20;
		if (respawnparm)
		    netbuffer->retransmitfrom |= 0x10;
		netbuffer->starttic = startepisode * 64 + startmap;
		netbuffer->player = VERSION;
		netbuffer->numtics = 0;
		HSendPacket (i, NCMD_SETUP);
	    }

#if 1
	    for(i = 10 ; i  &&  HGetPacket(); --i)
	    {
		if((netbuffer->player&0x7f) < MAXNETNODES)
		    gotinfo[netbuffer->player&0x7f] = true;
	    }
#else
	    while (HGetPacket ())
	    {
		gotinfo[netbuffer->player&0x7f] = true;
	    }
#endif

	    for (i=1 ; i<doomcom->numnodes ; i++)
		if (!gotinfo[i])
		    break;
	} while (i < doomcom->numnodes);
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme répartiteur alternatif dans Factorio. Il comme un répartiteur qui dirige les ressources vers un chemin alternatif.*

## Patterns Similaires
- [[else_DOOM_fe2f050f|f_finale.c:415]] (F_CastTicker)
- [[else_DOOM_3d23fea9|g_game.c:933]] (global)
- [[else_DOOM_1b8a24c7|i_sound.c:807]] (I_InitSound)
- [[else_DOOM_abd594b5|i_video.c:504]] (global)
- [[else_DOOM_cd5698e2|p_doors.c:649]] (global)

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
