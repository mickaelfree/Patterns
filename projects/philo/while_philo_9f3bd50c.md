---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: main.c
line: 60
project: philo
first_seen: 2025-05-07
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `main.c`
- **Ligne**: 60
- **Fonction**: ft_sleep
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (t_sleep > duration)
	{
		if (duration - last_dif > check_point)
		{
			printf("%ld\tseconde\n", duration / 1000);
			// divise par 1000 pour avoir des seconde
			last_dif = duration;
		}
		// usleep(50); Inutile pour linstant
		duration = get_time_pass(data->t_start, &(data->err)) - pass_s_fix;
		if (data->err)
			return (0);
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
- [[while_philo_60e2f99f|time.c:51]] (ft_sleep)
- [[while_philo_60e2f99f|time.c:51]] (ft_sleep)

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
