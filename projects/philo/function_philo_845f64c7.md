---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_thread.c
line: 50
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_thread.c`
- **Ligne**: 50
- **Fonction**: on_or_off_all_thread
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
Faire une boucle qui verifie pour chaque philo si ils ont pas deppase leur t_death
int	is_dead(t_data *d)
{
	int		i;
	t_philo	*p;
	long	duration;

	i = 0;
	while (d->all_philo[i])
	{
		p = d->all_philo[i++];
		duration = get_time_pass(d->t_start, &(d->err));
		if (d->err)
			return (1);
		if (duration - p->t_last_eat >= d->t_die)
		{
			ft_message(get_time_pass(p->data->t_start, &(p->data->err)), p->id, "died", d);
			pthread_mutex_lock(d->check);
			d->finish = 1;
			d->evryone_is_alive = FALSE;
			pthread_mutex_unlock(d->check);
			return (1);
		}
	}
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_da92a3f5|init_thread.c:50]] (on_or_off_all_thread)

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
