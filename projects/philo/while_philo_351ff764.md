---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: init_bonus.c
line: 22
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `init_bonus.c`
- **Ligne**: 22
- **Fonction**: init_philos
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (++i < count)
	{
		philos[i] = (t_philo *)malloc(sizeof(t_philo));
		if (!philos[i])
			destroy_all(engine, "[Malloc ERROR]\n", true, EXIT_FAILURE);
		philos[i]->id = i + 1;
		philos[i]->sems = engine->sems;
		philos[i]->times.die = ft_atoi(argv[2]);
		philos[i]->times.eat = ft_atoi(argv[3]);
		philos[i]->times.sleep = ft_atoi(argv[4]);
		philos[i]->times.last_meal = get_current_time();
		philos[i]->times.born_time = get_current_time();
		philos[i]->must_eat = -1;
		if (argv[5])
			philos[i]->must_eat = ft_atoi(argv[5]);
		philos[i]->meals_eaten = 0;
		philos[i]->philo_count = count;
	}
```

## Analyse Structurelle
**Type détecté**: Risque de tournage infini

Attention: Cette boucle pourrait être infinie si la condition n'est jamais modifiée dans le corps.

**Analogie Factorio**:
Comme un tapis roulant sans condition d'arrêt qui risque de tourner indéfiniment et bloquer votre usine.

## Note Factorio-style
*Ce pattern fonctionne comme tapis roulant surveillé dans Factorio. Il comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
*Aucun pattern lié trouvé*
