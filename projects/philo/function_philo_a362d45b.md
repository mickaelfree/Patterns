---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: main.c
line: 30
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `main.c`
- **Ligne**: 30
- **Fonction**: main
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	main(int argc, char **argv)
{
	t_data	*data;
	int		i;
	i = -1;
	data = init_data(argc, argv);
	if (!data || data->err)
		return (end(data, 1));

	data->nbr_thread_actif = 0;
	//Création des threads
	while (++i < data->n_philo)
	{
		if (pthread_create(&(data->threads[i]), \
		NULL, thread_philo, data->all_philo[i]))
			return(end(data, 4));
//return une erreur si pb a la creation
	}
	//attendre la fin des threads
	i = -1;
	while (++i < data->n_philo)
	{
		if (pthread_join(data->threads[i], NULL) != 0)
			return(end(data, 5));
	}
	//Fin d'execution des threads
	printf("NBR de thread actif = %d\n", data->nbr_thread_actif);
	return (end(data, data->err));
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_5ee8367f|main.c:76]] (ft_sleep)
- [[function_philo_db53e8fc|main.c:15]] (main)
- [[function_philo_db53e8fc|main.c:15]] (main)
- [[function_philo_db53e8fc|main.c:15]] (main)
- [[function_philo_d788c67e|main.c:15]] (main)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
