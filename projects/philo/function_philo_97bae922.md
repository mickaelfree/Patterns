---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: eat_sleep_think.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `eat_sleep_think.c`
- **Ligne**: 15
- **Fonction**: ft_eat
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	ft_eat(t_philo *philo, t_data *data)
{
	if (!is_finish(data))
		return (give_fork(philo, data), 1);
	ft_message(philo, "is eating", data->mutexs);
	pthread_mutex_lock(data->mutexs.eat);
	philo->nbr_eat++;
	philo->t_last_eat = get_time_pass(data->t_start);
	pthread_mutex_unlock(data->mutexs.eat);
	ft_sleep(data->param.t_eat);
	give_fork(philo, data);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_cb9b634c|eat.c:15]] (ft_eat)
- [[function_philo_57e82367|eat.c:15]] (ft_eat)
- [[function_philo_272008d6|eat_sleep_think.c:36]] (philo_sleep)
- [[function_philo_f487c63f|eat_sleep_think.c:36]] (philo_sleep)
- [[function_philo_10434119|eat_sleep_think.c:29]] (ft_eat)

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
