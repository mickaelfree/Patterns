---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: check.c
line: 57
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 57
- **Fonction**: evryone_eat
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	check_all_thread(t_data *d, t_parametre p, t_all_mutex m)
{
	int		finish;
	int		i;
	t_philo	*philo;
	long	duration;

	finish = FALSE;
	while (!finish)
	{
		i = 0;
		while (!finish && d->all_philo[i])
		{
			philo = d->all_philo[i++];
			duration = get_time_pass(d->t_start, &(d->err));
			if (d->err)
				finish = TRUE;
			if (la_morgue(philo, p, m, duration))
				finish = TRUE;
		}
		if (evryone_eat(d, p, m))
			finish = TRUE ;
		pthread_mutex_lock(m.check);
		if (d->err)
			finish = TRUE;
		pthread_mutex_unlock(m.check);
	}
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_31ab95cb|check.c:55]] (evryone_eat)
- [[function_philo_31ab95cb|check.c:55]] (evryone_eat)

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
