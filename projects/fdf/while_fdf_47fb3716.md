---
tags: pattern, pattern/while, factorio, code-logic, project/fdf, pattern/variant/potential_infinite
date: 2025-04-25
pattern_type: while
pattern_variant: potential_infinite
source_file: split.c
line: 57
project: fdf
first_seen: 2025-04-25
occurrences: 11
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `split.c`
- **Ligne**: 57
- **Fonction**: free_tab
- **Projet**: fdf
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (i < w)
	{
		free(tab[i]);
		i++;
	}
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_fdf_b27ffe22|get_next_line_utils.c:32]] (global)
- [[while_fdf_37e61a91|fdf3.c:184]] (get_width)
- [[while_fdf_fd5a0011|get_next_line_utils.c:27]] (global)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 11 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[for_fdf_aa045c10|🔄 Chaîne de montage (FOR)]]
[[for_fdf_b3efebf6|🔄 Chaîne de montage (FOR)]]
[[for_fdf_c97cbea4|🔄 Chaîne de montage (FOR)]]
