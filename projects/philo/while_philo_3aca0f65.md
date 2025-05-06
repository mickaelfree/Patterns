---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: init_mutex.c
line: 20
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `init_mutex.c`
- **Ligne**: 20
- **Fonction**: init_all_fork
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (!(*err) && ++i < nombre_de_philo)
	{
		mutexs->all_fork[i] = ft_calloc(1, sizeof(pthread_mutex_t));
		if (pthread_mutex_init(mutexs->all_fork[i], NULL))
			*err = 6;
	}
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Patterns Similaires
- [[while_philo_f410a7d5|init_mutex.c:20]] (init_all_fork)
- [[while_philo_c32b0efa|init_free_all_mutex.c:25]] (init_all_fork)
- [[while_philo_c32b0efa|init_free_all_mutex.c:25]] (init_all_fork)
- [[while_philo_adb68ed0|init_mutex.c:32]] (free_all_fork)
- [[while_philo_adb68ed0|init_mutex.c:32]] (free_all_fork)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 3 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
*Aucun pattern lié trouvé*
