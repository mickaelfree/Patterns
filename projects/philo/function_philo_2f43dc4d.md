---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_data.c
line: 15
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_data.c`
- **Ligne**: 15
- **Fonction**: init_data
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	init_data(t_data **data, int argc, char **argv)
{
	t_data	*d;

	*(data) = ft_calloc(1, sizeof(t_data));
	if (*data == NULL)
		return (1);
	d = *(data);
	d->err = 0;
	d->evryone_is_alive = TRUE;
	d->one_dead = FALSE;
	d->param = init_parsing(&(d->err), argc, argv);
	d->mutexs = init_mutex(&(d->err), d->param.n_philo);
	d->threads = init_thread(d);
	d->all_philo = ft_init_all_philo(d);
	if (!d->err && gettimeofday(&(d->t_start), NULL) == -1)
		d->err = 5;
	return (d->err);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_106ebbd4|init_free_data.c:15]] (init_data)
- [[function_philo_106ebbd4|init_free_data.c:15]] (init_data)
- [[function_philo_d4484d40|init_data.c:15]] (init_data)
- [[function_philo_d4484d40|init_data.c:15]] (init_data)
- [[function_philo_b40b1bc3|init_data.c:15]] (init_data)

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
