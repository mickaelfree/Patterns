---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: gestion_thread.c
line: 77
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `gestion_thread.c`
- **Ligne**: 77
- **Fonction**: toujour_a_table
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	thread_gestion(t_data *data)
{
	int		i;
	t_philo	*philo;

	i = -1;
	while (++i < data->param.n_philo)
	{
		philo = data->all_philo[i];
		if (pthread_create(&(data->threads[i]), NULL, routine, philo))
			data->err = 7;
	}
	toujour_a_table(data);
	i = -1;
	while (++i < data->param.n_philo)
	{
		if (pthread_join(data->threads[i], NULL) != 0)
			data->err = 8;
	}
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_08c8454e|check.c:86]] (check_all_thread)
- [[function_philo_52da9b40|check.c:82]] (cheack_all_thread)
- [[function_philo_52da9b40|check.c:82]] (cheack_all_thread)
- [[function_philo_5d05b076|init_philo.c:50]] (free_philo)
- [[function_philo_5d05b076|init_philo.c:50]] (free_philo)

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
