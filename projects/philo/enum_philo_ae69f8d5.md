---
tags: pattern, pattern/enum, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: enum
pattern_variant: simple
source_file: philo_bonus.h
line: 116
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🔢 Palette de ressources (ENUM) (Simple)

## Contexte
- **Fichier**: `philo_bonus.h`
- **Ligne**: 116
- **Fonction**: Aucune (niveau global)
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔢 **Palette de ressources**

Comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.

## Code Source
```c
enum e_status
{
	DIED = 0,
	EATING = 1,
	SLEEPING = 2,
	THINKING = 3,
	GOT_FORK_1 = 4,
	GOT_FORK_2 = 5
}
```

## Note Factorio-style
*Ce pattern fonctionne comme palette de ressources dans Factorio. Il comme un ensemble d'options prédéfinies, similaire à un réseau logique à constantes.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
*Aucun pattern lié trouvé*
