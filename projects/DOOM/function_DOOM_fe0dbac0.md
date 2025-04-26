---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: soundsrv.c
line: 142
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `soundsrv.c`
- **Ligne**: 142
- **Fonction**: derror
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int mix(void)
{

    register int		dl;
    register int		dr;
    register unsigned int	sample;
    
    signed short*		leftout;
    signed short*		rightout;
    signed short*		leftend;
    
    int				step;

    leftout = mixbuffer;
    rightout = mixbuffer+1;
    step = 2;

    leftend = mixbuffer + SAMPLECOUNT*step;

    // mix into the mixing buffer
    while (leftout != leftend)
    {

	dl = 0;
	dr = 0;

	if (channels[0])
	{
	    sample = *channels[0];
	    dl += channelleftvol_lookup[0][sample];
	    dr += channelrightvol_lookup[0][sample];
	    channelstepremainder[0] += channelstep[0];
	    channels[0] += channelstepremainder[0] >> 16;
	    channelstepremainder[0] &= 65536-1;

	    if (channels[0] >= channelsend[0])
		channels[0] = 0;
	}

	if (channels[1])
	{
	    sample = *channels[1];
	    dl += channelleftvol_lookup[1][sample];
	    dr += channelrightvol_lookup[1][sample];
	    channelstepremainder[1] += channelstep[1];
	    channels[1] += channelstepremainder[1] >> 16;
	    channelstepremainder[1] &= 65536-1;

	    if (channels[1] >= channelsend[1])
		channels[1] = 0;
	}

	if (channels[2])
	{
	    sample = *channels[2];
	    dl += channelleftvol_lookup[2][sample];
	    dr += channelrightvol_lookup[2][sample];
	    channelstepremainder[2] += channelstep[2];
	    channels[2] += channelstepremainder[2] >> 16;
	    channelstepremainder[2] &= 65536-1;

	    if (channels[2] >= channelsend[2])
		channels[2] = 0;
	}
	
	if (channels[3])
	{
	    sample = *channels[3];
	    dl += channelleftvol_lookup[3][sample];
	    dr += channelrightvol_lookup[3][sample];
	    channelstepremainder[3] += channelstep[3];
	    channels[3] += channelstepremainder[3] >> 16;
	    channelstepremainder[3] &= 65536-1;

	    if (channels[3] >= channelsend[3])
		channels[3] = 0;
	}
	
	if (channels[4])
	{
	    sample = *channels[4];
	    dl += channelleftvol_lookup[4][sample];
	    dr += channelrightvol_lookup[4][sample];
	    channelstepremainder[4] += channelstep[4];
	    channels[4] += channelstepremainder[4] >> 16;
	    channelstepremainder[4] &= 65536-1;

	    if (channels[4] >= channelsend[4])
		channels[4] = 0;
	}
	
	if (channels[5])
	{
	    sample = *channels[5];
	    dl += channelleftvol_lookup[5][sample];
	    dr += channelrightvol_lookup[5][sample];
	    channelstepremainder[5] += channelstep[5];
	    channels[5] += channelstepremainder[5] >> 16;
	    channelstepremainder[5] &= 65536-1;

	    if (channels[5] >= channelsend[5])
		channels[5] = 0;
	}
	
	if (channels[6])
	{
	    sample = *channels[6];
	    dl += channelleftvol_lookup[6][sample];
	    dr += channelrightvol_lookup[6][sample];
	    channelstepremainder[6] += channelstep[6];
	    channels[6] += channelstepremainder[6] >> 16;
	    channelstepremainder[6] &= 65536-1;

	    if (channels[6] >= channelsend[6])
		channels[6] = 0;
	}
	if (channels[7])
	{
	    sample = *channels[7];
	    dl += channelleftvol_lookup[7][sample];
	    dr += channelrightvol_lookup[7][sample];
	    channelstepremainder[7] += channelstep[7];
	    channels[7] += channelstepremainder[7] >> 16;
	    channelstepremainder[7] &= 65536-1;

	    if (channels[7] >= channelsend[7])
		channels[7] = 0;
	}

	// Has been char instead of short.
	// if (dl > 127) *leftout = 127;
	// else if (dl < -128) *leftout = -128;
	// else *leftout = dl;

	// if (dr > 127) *rightout = 127;
	// else if (dr < -128) *rightout = -128;
	// else *rightout = dr;
	
	if (dl > 0x7fff)
	    *leftout = 0x7fff;
	else if (dl < -0x8000)
	    *leftout = -0x8000;
	else
	    *leftout = dl;

	if (dr > 0x7fff)
	    *rightout = 0x7fff;
	else if (dr < -0x8000)
	    *rightout = -0x8000;
	else
	    *rightout = dr;

	leftout += step;
	rightout += step;

    }
    return 1;
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
