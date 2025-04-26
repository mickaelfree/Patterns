---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: s_sound.c
line: 827
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `s_sound.c`
- **Ligne**: 827
- **Fonction**: S_getChannel
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int
S_getChannel
( void*		origin,
  sfxinfo_t*	sfxinfo )
{
    // channel number to use
    int		cnum;
    
    channel_t*	c;

    // Find an open channel
    for (cnum=0 ; cnum<numChannels ; cnum++)
    {
	if (!channels[cnum].sfxinfo)
	    break;
	else if (origin &&  channels[cnum].origin ==  origin)
	{
	    S_StopChannel(cnum);
	    break;
	}
    }

    // None available
    if (cnum == numChannels)
    {
	// Look for lower priority
	for (cnum=0 ; cnum<numChannels ; cnum++)
	    if (channels[cnum].sfxinfo->priority >= sfxinfo->priority) break;

	if (cnum == numChannels)
	{
	    // FUCK!  No lower priority.  Sorry, Charlie.    
	    return -1;
	}
	else
	{
	    // Otherwise, kick out lower priority.
	    S_StopChannel(cnum);
	}
    }

    c = &channels[cnum];

    // channel is decided to be cnum.
    c->sfxinfo = sfxinfo;
    c->origin = origin;

    return cnum;
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
