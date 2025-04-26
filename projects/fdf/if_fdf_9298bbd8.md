---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/redundant
date: 2025-04-25
pattern_type: if
pattern_variant: redundant
source_file: fdf.c
line: 216
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteurs redondants)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 216
- **Fonction**: my_mlx_pixel_put
- **Projet**: fdf
- **Variante**: Capteurs redondants
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (x >= 0 && x < WIDTH && y >= 0 && y < HEIGHT)
	{
		dst = data->addr + (y * data->line_length + x * (data->bits_per_pixel / 8));
		*(unsigned int *)dst = color;
	}
```

## Analyse Structurelle
**Type détecté**: Capteurs redondants

Vérifiez les conditions potentiellement redondantes qui testent la même variable plusieurs fois.

**Analogie Factorio**:
Comme plusieurs capteurs qui mesurent la même ressource - un seul capteur bien configuré suffirait.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_fdf_1041c8ff|🔀 Répartiteur alternatif (ELSE)]]
[[else_fdf_16c235a8|🔀 Répartiteur alternatif (ELSE)]]
