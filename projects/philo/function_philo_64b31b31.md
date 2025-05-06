---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: take_fork.c
line: 74
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `take_fork.c`
- **Ligne**: 74
- **Fonction**: get_first_fork
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	ft_take_fork(t_philo *philo, t_data *d, t_parametre p, t_all_mutex m)
{
	if (!is_finish(d, m, philo))
		return (1);
	get_first_fork(philo, p, m);
	ft_message(get_time_pass(d->t_start, &(d->err)), philo, "has taken a fork 1 (faudra retirer le 1 et 2)", m);
	if (p.n_philo != 1)
	{
		get_second_fork(philo, p, m);
		ft_message(get_time_pass(d->t_start, &(d->err)), philo, "has taken a fork 2", m);
	}
	else
		ft_sleep(d, m, p.t_die);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_9d4a2e9f|take_fork.c:51]] (give_fork)
- [[function_philo_4176d21f|sleep.c:15]] (philo_sleep)
- [[function_philo_1ed5040c|sleep.c:15]] (philo_sleep)
- [[function_philo_96fdbe13|sleep.c:22]] (philo_sleep)

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
