---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_philo.c
line: 28
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_philo.c`
- **Ligne**: 28
- **Fonction**: get_second_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	get_first_fork(int id, t_parametre p)
{
	int	index_fork;

	if (id % 2 == 0)
		index_fork = id;
	else
		index_fork = id + 1;
	if (index_fork == p.n_philo)
		index_fork = 0;
	return (index_fork);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_545ba396|init_free_philo.c:28]] (get_second_fork)
- [[function_philo_545ba396|init_free_philo.c:28]] (get_second_fork)
- [[function_philo_8f4513c6|init_philo.c:15]] (get_second_fork)
- [[function_philo_8f4513c6|init_philo.c:15]] (get_second_fork)
- [[function_philo_a9a23d19|init_free_philo.c:15]] (get_second_fork)

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
