---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: init_mutex.c
line: 71
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 71
- **Fonction**: init_mutex
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void	free_mutex(t_all_mutex mutexs)
{
	if (mutexs.use_printf)
		pthread_mutex_destroy(mutexs.use_printf);
	free(mutexs.use_printf);
	mutexs.use_printf = NULL;
	if (mutexs.check)
		pthread_mutex_destroy(mutexs.check);
	free(mutexs.check);
	mutexs.check = NULL;
	if (mutexs.eat)
		pthread_mutex_destroy(mutexs.eat);
	free(mutexs.eat);
	mutexs.eat = NULL;
	free_all_fork(mutexs, -1);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_8b6bd670|init_free_all_mutex.c:81]] (init_all_mutex)
- [[function_philo_8b6bd670|init_free_all_mutex.c:81]] (init_all_mutex)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 3 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
