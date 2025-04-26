---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: split.c
line: 16
project: fdf
first_seen: 2025-04-25
occurrences: 14
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `split.c`
- **Ligne**: 16
- **Fonction**: ft_strlcpy
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
size_t	ft_strlcpy(char *dst, const char *src, size_t sz)
{
	const char	*s;
	size_t		len;

	s = src;
	while (*s)
		s++;
	len = s - src;
	if (!sz || !dst || !src)
		return (len);
	s = src;
	while (--sz && *s)
		*dst++ = *s++;
	*dst = '\0';
	return (len);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 14 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_fdf_2a890ee3|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_3fed850e|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_b83d5c36|🚚 Convoyeur de sortie (RETURN)]]
