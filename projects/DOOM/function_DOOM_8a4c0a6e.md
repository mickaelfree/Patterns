---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_inter.c
line: 338
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_inter.c`
- **Ligne**: 338
- **Fonction**: P_TouchSpecialThing
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
P_TouchSpecialThing
( mobj_t*	special,
  mobj_t*	toucher )
{
    player_t*	player;
    int		i;
    fixed_t	delta;
    int		sound;
		
    delta = special->z - toucher->z;

    if (delta > toucher->height
	|| delta < -8*FRACUNIT)
    {
	// out of reach
	return;
    }
    
	
    sound = sfx_itemup;	
    player = toucher->player;

    // Dead thing touching.
    // Can happen with a sliding player corpse.
    if (toucher->health <= 0)
	return;

    // Identify by sprite.
    switch (special->sprite)
    {
	// armor
      case SPR_ARM1:
	if (!P_GiveArmor (player, 1))
	    return;
	player->message = GOTARMOR;
	break;
		
      case SPR_ARM2:
	if (!P_GiveArmor (player, 2))
	    return;
	player->message = GOTMEGA;
	break;
	
	// bonus items
      case SPR_BON1:
	player->health++;		// can go over 100%
	if (player->health > 200)
	    player->health = 200;
	player->mo->health = player->health;
	player->message = GOTHTHBONUS;
	break;
	
      case SPR_BON2:
	player->armorpoints++;		// can go over 100%
	if (player->armorpoints > 200)
	    player->armorpoints = 200;
	if (!player->armortype)
	    player->armortype = 1;
	player->message = GOTARMBONUS;
	break;
	
      case SPR_SOUL:
	player->health += 100;
	if (player->health > 200)
	    player->health = 200;
	player->mo->health = player->health;
	player->message = GOTSUPER;
	sound = sfx_getpow;
	break;
	
      case SPR_MEGA:
	if (gamemode != commercial)
	    return;
	player->health = 200;
	player->mo->health = player->health;
	P_GiveArmor (player,2);
	player->message = GOTMSPHERE;
	sound = sfx_getpow;
	break;
	
	// cards
	// leave cards for everyone
      case SPR_BKEY:
	if (!player->cards[it_bluecard])
	    player->message = GOTBLUECARD;
	P_GiveCard (player, it_bluecard);
	if (!netgame)
	    break;
	return;
	
      case SPR_YKEY:
	if (!player->cards[it_yellowcard])
	    player->message = GOTYELWCARD;
	P_GiveCard (player, it_yellowcard);
	if (!netgame)
	    break;
	return;
	
      case SPR_RKEY:
	if (!player->cards[it_redcard])
	    player->message = GOTREDCARD;
	P_GiveCard (player, it_redcard);
	if (!netgame)
	    break;
	return;
	
      case SPR_BSKU:
	if (!player->cards[it_blueskull])
	    player->message = GOTBLUESKUL;
	P_GiveCard (player, it_blueskull);
	if (!netgame)
	    break;
	return;
	
      case SPR_YSKU:
	if (!player->cards[it_yellowskull])
	    player->message = GOTYELWSKUL;
	P_GiveCard (player, it_yellowskull);
	if (!netgame)
	    break;
	return;
	
      case SPR_RSKU:
	if (!player->cards[it_redskull])
	    player->message = GOTREDSKULL;
	P_GiveCard (player, it_redskull);
	if (!netgame)
	    break;
	return;
	
	// medikits, heals
      case SPR_STIM:
	if (!P_GiveBody (player, 10))
	    return;
	player->message = GOTSTIM;
	break;
	
      case SPR_MEDI:
	if (!P_GiveBody (player, 25))
	    return;

	if (player->health < 25)
	    player->message = GOTMEDINEED;
	else
	    player->message = GOTMEDIKIT;
	break;

	
	// power ups
      case SPR_PINV:
	if (!P_GivePower (player, pw_invulnerability))
	    return;
	player->message = GOTINVUL;
	sound = sfx_getpow;
	break;
	
      case SPR_PSTR:
	if (!P_GivePower (player, pw_strength))
	    return;
	player->message = GOTBERSERK;
	if (player->readyweapon != wp_fist)
	    player->pendingweapon = wp_fist;
	sound = sfx_getpow;
	break;
	
      case SPR_PINS:
	if (!P_GivePower (player, pw_invisibility))
	    return;
	player->message = GOTINVIS;
	sound = sfx_getpow;
	break;
	
      case SPR_SUIT:
	if (!P_GivePower (player, pw_ironfeet))
	    return;
	player->message = GOTSUIT;
	sound = sfx_getpow;
	break;
	
      case SPR_PMAP:
	if (!P_GivePower (player, pw_allmap))
	    return;
	player->message = GOTMAP;
	sound = sfx_getpow;
	break;
	
      case SPR_PVIS:
	if (!P_GivePower (player, pw_infrared))
	    return;
	player->message = GOTVISOR;
	sound = sfx_getpow;
	break;
	
	// ammo
      case SPR_CLIP:
	if (special->flags & MF_DROPPED)
	{
	    if (!P_GiveAmmo (player,am_clip,0))
		return;
	}
	else
	{
	    if (!P_GiveAmmo (player,am_clip,1))
		return;
	}
	player->message = GOTCLIP;
	break;
	
      case SPR_AMMO:
	if (!P_GiveAmmo (player, am_clip,5))
	    return;
	player->message = GOTCLIPBOX;
	break;
	
      case SPR_ROCK:
	if (!P_GiveAmmo (player, am_misl,1))
	    return;
	player->message = GOTROCKET;
	break;
	
      case SPR_BROK:
	if (!P_GiveAmmo (player, am_misl,5))
	    return;
	player->message = GOTROCKBOX;
	break;
	
      case SPR_CELL:
	if (!P_GiveAmmo (player, am_cell,1))
	    return;
	player->message = GOTCELL;
	break;
	
      case SPR_CELP:
	if (!P_GiveAmmo (player, am_cell,5))
	    return;
	player->message = GOTCELLBOX;
	break;
	
      case SPR_SHEL:
	if (!P_GiveAmmo (player, am_shell,1))
	    return;
	player->message = GOTSHELLS;
	break;
	
      case SPR_SBOX:
	if (!P_GiveAmmo (player, am_shell,5))
	    return;
	player->message = GOTSHELLBOX;
	break;
	
      case SPR_BPAK:
	if (!player->backpack)
	{
	    for (i=0 ; i<NUMAMMO ; i++)
		player->maxammo[i] *= 2;
	    player->backpack = true;
	}
	for (i=0 ; i<NUMAMMO ; i++)
	    P_GiveAmmo (player, i, 1);
	player->message = GOTBACKPACK;
	break;
	
	// weapons
      case SPR_BFUG:
	if (!P_GiveWeapon (player, wp_bfg, false) )
	    return;
	player->message = GOTBFG9000;
	sound = sfx_wpnup;	
	break;
	
      case SPR_MGUN:
	if (!P_GiveWeapon (player, wp_chaingun, special->flags&MF_DROPPED) )
	    return;
	player->message = GOTCHAINGUN;
	sound = sfx_wpnup;	
	break;
	
      case SPR_CSAW:
	if (!P_GiveWeapon (player, wp_chainsaw, false) )
	    return;
	player->message = GOTCHAINSAW;
	sound = sfx_wpnup;	
	break;
	
      case SPR_LAUN:
	if (!P_GiveWeapon (player, wp_missile, false) )
	    return;
	player->message = GOTLAUNCHER;
	sound = sfx_wpnup;	
	break;
	
      case SPR_PLAS:
	if (!P_GiveWeapon (player, wp_plasma, false) )
	    return;
	player->message = GOTPLASMA;
	sound = sfx_wpnup;	
	break;
	
      case SPR_SHOT:
	if (!P_GiveWeapon (player, wp_shotgun, special->flags&MF_DROPPED ) )
	    return;
	player->message = GOTSHOTGUN;
	sound = sfx_wpnup;	
	break;
		
      case SPR_SGN2:
	if (!P_GiveWeapon (player, wp_supershotgun, special->flags&MF_DROPPED ) )
	    return;
	player->message = GOTSHOTGUN2;
	sound = sfx_wpnup;	
	break;
		
      default:
	I_Error ("P_SpecialThing: Unknown gettable thing");
    }
	
    if (special->flags & MF_COUNTITEM)
	player->itemcount++;
    P_RemoveMobj (special);
    player->bonuscount += BONUSADD;
    if (player == &players[consoleplayer])
	S_StartSound (NULL, sound);
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
