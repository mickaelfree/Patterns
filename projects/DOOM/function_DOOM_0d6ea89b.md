---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: g_game.c
line: 1364
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `g_game.c`
- **Ligne**: 1364
- **Fonction**: G_InitNew
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
G_InitNew
( skill_t	skill,
  int		episode,
  int		map ) 
{ 
    int             i; 
	 
    if (paused) 
    { 
	paused = false; 
	S_ResumeSound (); 
    } 
	

    if (skill > sk_nightmare) 
	skill = sk_nightmare;


    // This was quite messy with SPECIAL and commented parts.
    // Supposedly hacks to make the latest edition work.
    // It might not work properly.
    if (episode < 1)
      episode = 1; 

    if ( gamemode == retail )
    {
      if (episode > 4)
	episode = 4;
    }
    else if ( gamemode == shareware )
    {
      if (episode > 1) 
	   episode = 1;	// only start episode 1 on shareware
    }  
    else
    {
      if (episode > 3)
	episode = 3;
    }
    

  
    if (map < 1) 
	map = 1;
    
    if ( (map > 9)
	 && ( gamemode != commercial) )
      map = 9; 
		 
    M_ClearRandom (); 
	 
    if (skill == sk_nightmare || respawnparm )
	respawnmonsters = true;
    else
	respawnmonsters = false;
		
    if (fastparm || (skill == sk_nightmare && gameskill != sk_nightmare) )
    { 
	for (i=S_SARG_RUN1 ; i<=S_SARG_PAIN2 ; i++) 
	    states[i].tics >>= 1; 
	mobjinfo[MT_BRUISERSHOT].speed = 20*FRACUNIT; 
	mobjinfo[MT_HEADSHOT].speed = 20*FRACUNIT; 
	mobjinfo[MT_TROOPSHOT].speed = 20*FRACUNIT; 
    } 
    else if (skill != sk_nightmare && gameskill == sk_nightmare) 
    { 
	for (i=S_SARG_RUN1 ; i<=S_SARG_PAIN2 ; i++) 
	    states[i].tics <<= 1; 
	mobjinfo[MT_BRUISERSHOT].speed = 15*FRACUNIT; 
	mobjinfo[MT_HEADSHOT].speed = 10*FRACUNIT; 
	mobjinfo[MT_TROOPSHOT].speed = 10*FRACUNIT; 
    } 
	 
			 
    // force players to be initialized upon first level load         
    for (i=0 ; i<MAXPLAYERS ; i++) 
	players[i].playerstate = PST_REBORN; 
 
    usergame = true;                // will be set false if a demo 
    paused = false; 
    demoplayback = false; 
    automapactive = false; 
    viewactive = true; 
    gameepisode = episode; 
    gamemap = map; 
    gameskill = skill; 
 
    viewactive = true;
    
    // set the sky map for the episode
    if ( gamemode == commercial)
    {
	skytexture = R_TextureNumForName ("SKY3");
	if (gamemap < 12)
	    skytexture = R_TextureNumForName ("SKY1");
	else
	    if (gamemap < 21)
		skytexture = R_TextureNumForName ("SKY2");
    }
    else
	switch (episode) 
	{ 
	  case 1: 
	    skytexture = R_TextureNumForName ("SKY1"); 
	    break; 
	  case 2: 
	    skytexture = R_TextureNumForName ("SKY2"); 
	    break; 
	  case 3: 
	    skytexture = R_TextureNumForName ("SKY3"); 
	    break; 
	  case 4:	// Special Edition sky
	    skytexture = R_TextureNumForName ("SKY4");
	    break;
	} 
 
    G_DoLoadLevel (); 
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
