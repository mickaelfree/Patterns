---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: ft_calloc_and_time.c
line: 46
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `ft_calloc_and_time.c`
- **Ligne**: 46
- **Fonction**: get_time_pass
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
Renvoie le temp ecoule depuis start en microsecond
long	get_time_pass(struct timeval start)
{
	struct timeval	now;
	long			pass;

	gettimeofday(&(now), NULL);
	pass = now.tv_sec * 1000 + now.tv_usec / 1000;
	pass = pass - (start.tv_sec * 1000 + start.tv_usec / 1000);
	return (pass);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_48fe74c3|time.c:20]] (get_time_pass)
- [[function_philo_48fe74c3|time.c:20]] (get_time_pass)
- [[function_philo_48fe74c3|time.c:20]] (get_time_pass)
- [[function_philo_48fe74c3|time.c:20]] (get_time_pass)
- [[function_philo_48fe74c3|time.c:20]] (get_time_pass)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
