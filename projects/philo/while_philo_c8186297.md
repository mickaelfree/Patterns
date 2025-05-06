---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: gestion_thread.c
line: 42
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `gestion_thread.c`
- **Ligne**: 42
- **Fonction**: evryone_to_eat
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (data->all_philo[++i])
	{
		philo = data->all_philo[i];
		pthread_mutex_lock(data->mutexs.eat);
		if (data->param.n_eat == -1 || data->param.n_eat > philo->nbr_eat)
			return (pthread_mutex_unlock(data->mutexs.eat), 0);
		pthread_mutex_unlock(data->mutexs.eat);
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
- [[while_philo_4b500f47|check.c:44]] (evryone_eat)
- [[while_philo_4b500f47|check.c:44]] (evryone_eat)
- [[while_philo_4b500f47|check.c:44]] (evryone_eat)
- [[while_philo_6df29fbe|simulation.c:24]] (is_all_eat)

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
