---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_pspr.c
line: 577
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_pspr.c`
- **Ligne**: 577
- **Fonction**: A_FirePlasma
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
A_FirePlasma
( player_t*	player,
  pspdef_t*	psp ) 
{
    player->ammo[weaponinfo[player->readyweapon].ammo]--;

    P_SetPsprite (player,
		  ps_flash,
		  weaponinfo[player->readyweapon].flashstate+(P_Random ()&1) );

    P_SpawnPlayerMissile (player->mo, MT_PLASMA);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_f21347a4|p_pspr.c:550]] (A_FireMissile)
- [[function_DOOM_c6033d66|p_pspr.c:563]] (A_FireBFG)
- [[function_DOOM_fde2e254|p_pspr.c:448]] (A_GunFlash)
- [[function_DOOM_52e6c54f|p_pspr.c:646]] (A_FirePistol)
- [[function_DOOM_d5db03d9|p_pspr.c:668]] (A_FireShotgun)

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
