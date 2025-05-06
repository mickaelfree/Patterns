---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_philo.c
line: 60
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_philo.c`
- **Ligne**: 60
- **Fonction**: ft_init_all_philo
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	ft_init_all_philo(t_data *data)
{
	int		i;

	if (!data || data->err)
		return ;
	i = -1;
	data->all_philo = ft_calloc(data->param.n_philo, sizeof(t_philo));
	if (!data->all_philo)
		data->err = 1;
	while (data->all_philo && !data->err && ++i < data->param.n_philo)
		data->all_philo[i] = ft_init_philo(data, i);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_9613b853|init_philo.c:30]] (ft_init_all_philo)
- [[function_philo_9613b853|init_philo.c:30]] (ft_init_all_philo)
- [[function_philo_862a1ebb|init_thread.c:15]] (init_thread)
- [[function_philo_862a1ebb|init_thread.c:15]] (init_thread)
- [[function_philo_1f1cc8c8|init_thread.c:15]] (init_thread)

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
