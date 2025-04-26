---
tags: pattern, pattern/while, factorio, code-logic, project/DOOM, pattern/variant/potential_infinite
date: 2025-04-25
pattern_type: while
pattern_variant: potential_infinite
source_file: d_net.c
line: 269
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `d_net.c`
- **Ligne**: 269
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while ( HGetPacket() )
    {
	if (netbuffer->checksum & NCMD_SETUP)
	    continue;		// extra setup packet
			
	netconsole = netbuffer->player & ~PL_DRONE;
	netnode = doomcom->remotenode;
	
	// to save bytes, only the low byte of tic numbers are sent
	// Figure out what the rest of the bytes are
	realstart = ExpandTics (netbuffer->starttic);		
	realend = (realstart+netbuffer->numtics);
	
	// check for exiting the game
	if (netbuffer->checksum & NCMD_EXIT)
	{
	    if (!nodeingame[netnode])
		continue;
	    nodeingame[netnode] = false;
	    playeringame[netconsole] = false;
	    strcpy (exitmsg, "Player 1 left the game");
	    exitmsg[7] += netconsole;
	    players[consoleplayer].message = exitmsg;
	    if (demorecording)
		G_CheckDemoStatus ();
	    continue;
	}
	
	// check for a remote game kill
	if (netbuffer->checksum & NCMD_KILL)
	    I_Error ("Killed by network driver");

	nodeforplayer[netconsole] = netnode;
	
	// check for retransmit request
	if ( resendcount[netnode] <= 0 
	     && (netbuffer->checksum & NCMD_RETRANSMIT) )
	{
	    resendto[netnode] = ExpandTics(netbuffer->retransmitfrom);
	    if (debugfile)
		fprintf (debugfile,"retransmit from %i\n", resendto[netnode]);
	    resendcount[netnode] = RESENDCOUNT;
	}
	else
	    resendcount[netnode]--;
	
	// check for out of order / duplicated packet		
	if (realend == nettics[netnode])
	    continue;
			
	if (realend < nettics[netnode])
	{
	    if (debugfile)
		fprintf (debugfile,
			 "out of order packet (%i + %i)\n" ,
			 realstart,netbuffer->numtics);
	    continue;
	}
	
	// check for a missed packet
	if (realstart > nettics[netnode])
	{
	    // stop processing until the other system resends the missed tics
	    if (debugfile)
		fprintf (debugfile,
			 "missed tics from %i (%i - %i)\n",
			 netnode, realstart, nettics[netnode]);
	    remoteresend[netnode] = true;
	    continue;
	}

	// update command store from the packet
        {
	    int		start;

	    remoteresend[netnode] = false;
		
	    start = nettics[netnode] - realstart;		
	    src = &netbuffer->cmds[start];

	    while (nettics[netnode] < realend)
	    {
		dest = &netcmds[netconsole][nettics[netnode]%BACKUPTICS];
		nettics[netnode]++;
		*dest = *src;
		src++;
	    }
	}
    }
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_DOOM_d8387845|d_net.c:536]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[for_DOOM_b08db244|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_790f12f4|🔄 Chaîne de montage (FOR)]]
[[for_DOOM_fe5c5de5|🔄 Chaîne de montage (FOR)]]
[[do_while_DOOM_f95c2f34|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_b1640881|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_cd442d3d|🔄 Tapis roulant à activation garantie (DO WHILE)]]
