---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_mutex.c
line: 42
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 42
- **Fonction**: free_all_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	init_mutex(t_data *data)
{
	if (!data)
		return ;
	data->use_printf = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!data->use_printf)
		data->err = 1;
	else if (pthread_mutex_init(data->use_printf, NULL))
		data->err = 6;
	data->check = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!data->check)
		data->err = 1;
	else if (pthread_mutex_init(data->check, NULL))
		data->err = 6;
	data->eat = ft_calloc(1, sizeof(pthread_mutex_t));
	if (!data->eat)
		data->err = 1;
	else if (pthread_mutex_init(data->eat, NULL))
		data->err = 6;

	init_all_fork(data, -1);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_b06a4fbe|init_mutex.c:15]] (init_mutex)

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
