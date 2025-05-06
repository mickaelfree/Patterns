---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: parsing.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `parsing.c`
- **Ligne**: 15
- **Fonction**: ft_atoi
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	ft_atoi(char *s, int *error)
{
	size_t	i;
	long	res;

	if (!s || !s[0])
		return (*error = 3, 0);
	res = 0;
	i = 0;
	while (s[i])
	{
		if ((s[i] < '0' || s[i] > '9') || res > INT_MAX)
			return (*error = 4, 0);
		res = res * 10 + s[i++] - '0';
	}
	if (s[i] || res > INT_MAX)
		return (*error = 4, 0);
	return (res);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_04b21656|init_parsing.c:15]] (ft_atoi)
- [[function_philo_04b21656|init_parsing.c:15]] (ft_atoi)
- [[function_philo_a8a6f9aa|parsing.c:15]] (ft_atoi)
- [[function_philo_a8a6f9aa|parsing.c:15]] (ft_atoi)
- [[function_philo_a8a6f9aa|parsing.c:15]] (ft_atoi)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 5 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
