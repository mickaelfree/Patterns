---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: time.c
line: 38
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `time.c`
- **Ligne**: 38
- **Fonction**: ft_sleep
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
return 
long	ft_sleep(t_data *data, t_philo *philo, long t_sleep, long check_point)
{
	long	pass_s_fix;
	long	duration;
	long	last_dif;
	(void)	philo;

	pass_s_fix = get_time_pass(data->t_start, &(data->err));
	duration = get_time_pass(data->t_start, &(data->err)) - pass_s_fix;
	if (data->err)
		return (-1);
	last_dif = duration;
	while (t_sleep > duration)
	{
		if (duration - last_dif > check_point)
		{
			printf("%ld\tseconde\n", duration / 1000);
			last_dif = duration;
		}
		duration = get_time_pass(data->t_start, &(data->err)) - pass_s_fix;
		if (data->err)
			return (0);
	}
	return (duration);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_3f37fec4|time.c:34]] (get_time_pass)
- [[function_philo_8a359be6|main.c:49]] (get_time_pass)

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
