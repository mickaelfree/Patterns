---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: hu_lib.c
line: 305
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `hu_lib.c`
- **Ligne**: 305
- **Fonction**: HUlib_resetIText
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
HUlib_addPrefixToIText
( hu_itext_t*	it,
  char*		str )
{
    while (*str)
	HUlib_addCharToTextLine(&it->l, *(str++));
    it->lm = it->l.len;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_DOOM_508fd59e|hu_lib.c:292]] (HUlib_delCharFromIText)
- [[function_DOOM_277e0b9d|hu_lib.c:347]] (HUlib_drawIText)
- [[function_DOOM_1e2a5687|hu_lib.c:298]] (HUlib_eraseLineFromIText)
- [[function_DOOM_35f2fb8f|hu_lib.c:336]] (HUlib_keyInIText)
- [[function_DOOM_9a206cf6|hu_lib.c:231]] (HUlib_addMessageToSText)

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
