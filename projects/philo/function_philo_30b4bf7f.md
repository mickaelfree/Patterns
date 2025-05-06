---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: sleep.c
line: 22
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `sleep.c`
- **Ligne**: 22
- **Fonction**: philo_sleep
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	philo_think(t_philo *philo, t_data *d, t_all_mutex m)
{
	ft_message(d, philo, "is thinking", m);
	if (d->param.n_philo % 2 == 1)
		ft_sleep(d, m, d->param.t_eat / 2);
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_272008d6|eat_sleep_think.c:36]] (philo_sleep)
- [[function_philo_f487c63f|eat_sleep_think.c:36]] (philo_sleep)
- [[function_philo_df95f54b|sleep.c:15]] (philo_sleep)
- [[function_philo_10434119|eat_sleep_think.c:29]] (ft_eat)
- [[function_philo_cc9b5be6|eat_sleep_think.c:29]] (ft_eat)

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
