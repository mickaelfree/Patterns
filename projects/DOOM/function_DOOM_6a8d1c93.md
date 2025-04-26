---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: p_enemy.c
line: 1512
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `p_enemy.c`
- **Ligne**: 1512
- **Fonction**: A_PainAttack
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void A_PainAttack (mobj_t* actor)
{
    if (!actor->target)
	return;

    A_FaceTarget (actor);
    A_PainShootSkull (actor, actor->angle);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_4c840a03|p_enemy.c:969]] (A_HeadAttack)
- [[function_DOOM_3b2dcd44|p_enemy.c:898]] (A_SpidRefire)
- [[function_DOOM_951e8a0b|p_enemy.c:1093]] (A_Tracer)
- [[function_DOOM_eb1374e7|p_enemy.c:1002]] (A_SkelMissile)
- [[function_DOOM_614c8dfb|p_enemy.c:1577]] (A_XScream)

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
