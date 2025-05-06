---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: output.c
line: 110
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `output.c`
- **Ligne**: 110
- **Fonction**: write_outcome
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	write_outcome(t_table *table)
{
	unsigned int	i;
	unsigned int	full_count;

	full_count = 0;
	i = 0;
	while (i < table->nb_philos)
	{
		if (table->philos[i]->times_ate >= (unsigned int)table->must_eat_count)
			full_count++;
		i++;
	}
	pthread_mutex_lock(&table->write_lock);
	printf("%d/%d philosophers had at least %d meals.\n",
		full_count, table->nb_philos, table->must_eat_count);
	pthread_mutex_unlock(&table->write_lock);
	return ;
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
