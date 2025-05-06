---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: time.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 5
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `time.c`
- **Ligne**: 15
- **Fonction**: get_time_pass
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
long	get_time_pass(struct timeval start, int *error)
{
	struct timeval	now;
	long			pass;

	if (gettimeofday(&(now), NULL) == -1)
		return (*error = 5, 0);
	pass = now.tv_sec * 1000 + now.tv_usec / 1000;
	pass = pass - (start.tv_sec * 1000 + start.tv_usec / 1000);
	return (pass);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_69c08919|time.c:20]] (get_time_pass)
- [[function_philo_69c08919|time.c:20]] (get_time_pass)
- [[function_philo_99262539|time.c:19]] (get_time_in_ms)
- [[function_philo_99262539|time.c:19]] (get_time_in_ms)

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
