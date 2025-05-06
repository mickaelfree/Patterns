---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: message_and_end.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `message_and_end.c`
- **Ligne**: 15
- **Fonction**: ft_message
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
Printf si possible en respectant les mutexs
void	ft_message(t_philo *philo, char *message, t_all_mutex mutexs)
{
	long	time;

	time = get_time_pass(philo->data->t_start);
	pthread_mutex_lock(mutexs.check);
	if (philo->data->evryone_is_alive == TRUE)
	{
		pthread_mutex_unlock(mutexs.check);
		pthread_mutex_lock(mutexs.use_printf);
		if (philo->data->one_dead == FALSE)
			printf("%ld %d %s\n", time, philo->id + 1, message);
		pthread_mutex_unlock(mutexs.use_printf);
		return ;
	}
	pthread_mutex_unlock(mutexs.check);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_4c24bac2|message.c:15]] (ft_message)

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
