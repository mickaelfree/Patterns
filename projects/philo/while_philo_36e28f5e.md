---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: check.c
line: 91
project: philo
first_seen: 2025-05-07
occurrences: 3
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 91
- **Fonction**: thread_start
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (++i < d->param.n_philo)
	{
		if (pthread_create(&(d->threads[i]), NULL, routine, d->all_philo[i]))
			d->err = 7;
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
- [[while_philo_01c5ae85|gestion_thread.c:83]] (thread_gestion)
- [[while_philo_01c5ae85|gestion_thread.c:83]] (thread_gestion)
- [[while_philo_e8e4b6fe|check.c:94]] (thread_start)
- [[while_philo_e8e4b6fe|check.c:94]] (thread_start)
- [[while_philo_e8e4b6fe|check.c:94]] (thread_start)

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
