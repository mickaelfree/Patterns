---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: check.c
line: 61
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 61
- **Fonction**: evryone_eat
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	cheack_all_thread(t_data *d, t_parametre p, t_all_mutex m)
{
	int	vrai;
	int	i;
	t_philo	*philo;
	long	duration;

	vrai = TRUE;
	while (vrai)
	{
		i = 0;
		while (vrai && d->all_philo[i])
		{
			philo = d->all_philo[i++];
			duration = get_time_pass(d->t_start, &(d->err));
			if (d->err)
				vrai = FALSE;
			if (la_morgue(philo, p, m, duration))
				vrai = FALSE;
		}
		if (evryone_eat(d, p, m))
			vrai = FALSE ;
		if (d->err)
			vrai = FALSE ;
	}
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_5b4d7af6|check.c:57]] (evryone_eat)

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
