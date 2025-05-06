---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: check.c
line: 65
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `check.c`
- **Ligne**: 65
- **Fonction**: check_all_thread
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (!finish)
	{
		i = 0;
		while (!finish && d->all_philo[i])
		{
			philo = d->all_philo[i++];
			duration = get_time_pass(d->t_start, &(d->err));
			if (d->err)
				finish = TRUE;
			if (la_morgue(philo, p, m, duration))
				finish = TRUE;
		}
		if (evryone_eat(d, p, m))
			finish = TRUE ;
		pthread_mutex_lock(m.check);
		if (d->err)
			finish = TRUE;
		pthread_mutex_unlock(m.check);
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
- [[while_philo_03ea9fea|check.c:63]] (cheack_all_thread)
- [[while_philo_03ea9fea|check.c:63]] (cheack_all_thread)

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
