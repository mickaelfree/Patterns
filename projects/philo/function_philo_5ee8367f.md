---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: main.c
line: 76
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `main.c`
- **Ligne**: 76
- **Fonction**: ft_sleep
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
	int		error;
	long	passe_milis;

	error = 0;
	data = init_data(argc, argv, &error);
	if (error || !data->n_eat)
		return (end(data, error));
	// show_data(data);
	printf("START\n\n");
	passe_milis = ft_sleep(data, data->t_die, data->t_eat);
	printf("\n%ld seconde on ecoulé\n", passe_milis / 1000);
	// divise par 1000 pour avoir des seconde
	return (end(data, data->err));
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_19ec99f5|main.c:30]] (show_data)
- [[function_philo_a362d45b|main.c:30]] (main)
- [[function_philo_db53e8fc|main.c:15]] (main)
- [[function_philo_db53e8fc|main.c:15]] (main)
- [[function_philo_db53e8fc|main.c:15]] (main)

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
