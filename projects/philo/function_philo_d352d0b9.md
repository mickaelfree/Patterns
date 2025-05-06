---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_thread.c
line: 32
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_thread.c`
- **Ligne**: 32
- **Fonction**: free_thread
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	on_or_off_all_thread(t_data *data, int param)
{
	int	i;

	if (!data || data->err)
		return (1);
	i = -1;
	while (++i < data->n_philo)
	{
		if (param == ON && pthread_create(&(data->threads[i]), NULL, \
		thread_philo, data->all_philo[i]))
			return (data->err = 7, 1);
		else if (param == OFF && pthread_join(data->threads[i], NULL) != 0)
			return (data->err = 8, 1);
	}
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_5d05b076|init_philo.c:50]] (free_philo)
- [[function_philo_5d05b076|init_philo.c:50]] (free_philo)
- [[function_philo_5d05b076|init_philo.c:50]] (free_philo)
- [[function_philo_3b7ad477|gestion_thread.c:77]] (toujour_a_table)
- [[function_philo_3b7ad477|gestion_thread.c:77]] (toujour_a_table)

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
