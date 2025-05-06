---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: init_thread.c
line: 39
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `init_thread.c`
- **Ligne**: 39
- **Fonction**: on_or_off_all_thread
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (++i < data->n_philo)
	{
		if (param == ON && pthread_create(&(data->threads[i]), NULL, \
		thread_philo, data->all_philo[i]))
			return (data->err = 7, 1);
		else if (param == OFF && pthread_join(data->threads[i], NULL) != 0)
			return (data->err = 8, 1);
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
- [[while_philo_d796587f|main.c:71]] (main)
- [[while_philo_3659176a|main.c:41]] (main)
- [[while_philo_36e28f5e|check.c:87]] (thread_start)
- [[while_philo_36e28f5e|check.c:87]] (thread_start)
- [[while_philo_36e28f5e|check.c:87]] (thread_start)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
*Aucun pattern lié trouvé*
