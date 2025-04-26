---
tags: pattern, pattern/for, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: for
pattern_variant: simple
source_file: p_switch.c
line: 121
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🔄 Chaîne de montage (FOR) (Chaîne simple)

## Contexte
- **Fichier**: `p_switch.c`
- **Ligne**: 121
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Chaîne simple
- **Complexité**: standard

## Métaphore Factorio
🔄 **Chaîne de montage**

Comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.

## Code Source
```c
for (index = 0,i = 0;i < MAXSWITCHES;i++)
    {
	if (!alphSwitchList[i].episode)
	{
	    numswitches = index/2;
	    switchlist[index] = -1;
	    break;
	}
		
	if (alphSwitchList[i].episode <= episode)
	{
#if 0	// UNUSED - debug?
	    int		value;
			
	    if (R_CheckTextureNumForName(alphSwitchList[i].name1) < 0)
	    {
		I_Error("Can't find switch texture '%s'!",
			alphSwitchList[i].name1);
		continue;
	    }
	    
	    value = R_TextureNumForName(alphSwitchList[i].name1);
#endif
	    switchlist[index++] = R_TextureNumForName(alphSwitchList[i].name1);
	    switchlist[index++] = R_TextureNumForName(alphSwitchList[i].name2);
	}
    }
```

## Note Factorio-style
*Ce pattern fonctionne comme chaîne de montage dans Factorio. Il comme une chaîne de montage qui traite des éléments de façon séquentielle un nombre déterminé de fois.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[while_DOOM_669fd485|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_589dde27|⭕ Tapis roulant surveillé (WHILE)]]
[[while_DOOM_135bd103|⭕ Tapis roulant surveillé (WHILE)]]
[[do_while_DOOM_f95c2f34|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_b1640881|🔄 Tapis roulant à activation garantie (DO WHILE)]]
[[do_while_DOOM_cd442d3d|🔄 Tapis roulant à activation garantie (DO WHILE)]]
