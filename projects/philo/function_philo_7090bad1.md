---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: output.c
line: 42
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `output.c`
- **Ligne**: 42
- **Fonction**: write_status_debug
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static void	write_status_debug(t_philo *philo, t_status status)
{
	if (status == DIED)
		print_status_debug(philo, RED, "died", status);
	else if (status == EATING)
		print_status_debug(philo, GREEN, "is eating", status);
	else if (status == SLEEPING)
		print_status_debug(philo, CYAN, "is sleeping", status);
	else if (status == THINKING)
		print_status_debug(philo, CYAN, "is thinking", status);
	else if (status == GOT_FORK_1)
		print_status_debug(philo, PURPLE, "has taken a fork", status);
	else if (status == GOT_FORK_2)
		print_status_debug(philo, PURPLE, "has taken a fork", status);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

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
