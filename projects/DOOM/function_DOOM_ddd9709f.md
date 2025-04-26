---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: i_net.c
line: 161
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `i_net.c`
- **Ligne**: 161
- **Fonction**: PacketGet
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void PacketGet (void)
{
    int			i;
    int			c;
    struct sockaddr_in	fromaddress;
    int			fromlen;
    doomdata_t		sw;
				
    fromlen = sizeof(fromaddress);
    c = recvfrom (insocket, &sw, sizeof(sw), 0
		  , (struct sockaddr *)&fromaddress, &fromlen );
    if (c == -1 )
    {
	if (errno != EWOULDBLOCK)
	    I_Error ("GetPacket: %s",strerror(errno));
	doomcom->remotenode = -1;		// no packet
	return;
    }

    {
	static int first=1;
	if (first)
	    printf("len=%d:p=[0x%x 0x%x] \n", c, *(int*)&sw, *((int*)&sw+1));
	first = 0;
    }

    // find remote node number
    for (i=0 ; i<doomcom->numnodes ; i++)
	if ( fromaddress.sin_addr.s_addr == sendaddress[i].sin_addr.s_addr )
	    break;

    if (i == doomcom->numnodes)
    {
	// packet is not from one of the players (new game broadcast)
	doomcom->remotenode = -1;		// no packet
	return;
    }
	
    doomcom->remotenode = i;			// good packet from a game player
    doomcom->datalength = c;
	
    // byte swap
    netbuffer->checksum = ntohl(sw.checksum);
    netbuffer->player = sw.player;
    netbuffer->retransmitfrom = sw.retransmitfrom;
    netbuffer->starttic = sw.starttic;
    netbuffer->numtics = sw.numtics;

    for (c=0 ; c< netbuffer->numtics ; c++)
    {
	netbuffer->cmds[c].forwardmove = sw.cmds[c].forwardmove;
	netbuffer->cmds[c].sidemove = sw.cmds[c].sidemove;
	netbuffer->cmds[c].angleturn = ntohs(sw.cmds[c].angleturn);
	netbuffer->cmds[c].consistancy = ntohs(sw.cmds[c].consistancy);
	netbuffer->cmds[c].chatchar = sw.cmds[c].chatchar;
	netbuffer->cmds[c].buttons = sw.cmds[c].buttons;
    }
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_DOOM_3e1b4f0f|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
