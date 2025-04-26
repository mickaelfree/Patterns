---
tags: pattern, pattern/if, factorio, code-logic, project/fdf, pattern/variant/nested
date: 2025-04-25
pattern_type: if
pattern_variant: nested
source_file: split.c
line: 106
project: fdf
first_seen: 2025-04-25
occurrences: 11
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `split.c`
- **Ligne**: 106
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (*s != c)
		{
			len = 0;
			while (s[len] && s[len] != c)
				len++;
			tab = ft_tabword(tab, w++, s, c);
			if (!tab)
				return (NULL);
			s += len;
		}
```

## Analyse Structurelle
**Type détecté**: Capteur en cascade

Ces capteurs en cascade pourraient être combinés en un seul réseau logique avec des opérateurs && ou ||.

**Analogie Factorio**:
Comme plusieurs capteurs en série dans Factorio que vous pourriez remplacer par un circuit combinatoire unique.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 11 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_fdf_1041c8ff|🔀 Répartiteur alternatif (ELSE)]]
[[else_fdf_16c235a8|🔀 Répartiteur alternatif (ELSE)]]
