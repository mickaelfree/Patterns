---
tags: pattern, pattern/while, factorio, code-logic, project/philo, pattern/variant/potential_infinite
date: 2025-05-07
pattern_type: while
pattern_variant: potential_infinite
source_file: parsing.c
line: 25
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: oui
---

# ⭕ Tapis roulant surveillé (WHILE) (Risque de tournage infini)

## Contexte
- **Fichier**: `parsing.c`
- **Ligne**: 25
- **Fonction**: contains_only_digits
- **Projet**: philo
- **Variante**: Risque de tournage infini
- **Complexité**: risquée

## Métaphore Factorio
⭕ **Tapis roulant surveillé**

Comme un tapis roulant qui continue à fonctionner tant qu'une condition est vraie.

## Code Source
```c
while (str[i])
	{
		if (str[i] < '0' || str[i] > '9')
			return (false);
		i++;
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
- [[while_philo_1f5a22af|parsing.c:46]] (integer_atoi)
- [[while_philo_1f5a22af|parsing.c:46]] (integer_atoi)
- [[while_philo_e54efa32|parsing.c:24]] (ft_atoi)
- [[while_philo_f54b0e2a|parsing.c:24]] (ft_atoi)
- [[while_philo_f54b0e2a|parsing.c:24]] (ft_atoi)

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
