---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_pspr.c
line: 668
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_pspr.c`
- **Ligne**: 668
- **Fonction**: A_FireShotgun
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
A_FireShotgun
( player_t*	player,
  pspdef_t*	psp ) 
{
    int		i;
	
    S_StartSound (player->mo, sfx_shotgn);
    P_SetMobjState (player->mo, S_PLAY_ATK2);

    player->ammo[weaponinfo[player->readyweapon].ammo]--;

    P_SetPsprite (player,
		  ps_flash,
		  weaponinfo[player->readyweapon].flashstate);

    P_BulletSlope (player->mo);
	
    for (i=0 ; i<7 ; i++)
	P_GunShot (player->mo, false);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_3fdf9cd7|p_pspr.c:732]] (A_FireCGun)
- [[function_DOOM_0db85a12|p_pspr.c:695]] (A_FireShotgun2)
- [[function_DOOM_fde2e254|p_pspr.c:448]] (A_GunFlash)
- [[function_DOOM_b70f2d69|p_pspr.c:577]] (A_FirePlasma)
- [[function_DOOM_f21347a4|p_pspr.c:550]] (A_FireMissile)

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
