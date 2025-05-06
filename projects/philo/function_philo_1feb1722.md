---
tags: pattern, pattern/function, factorio, code-logic, project/philo, pattern/variant/simple
date: 2025-05-07
pattern_type: function
pattern_variant: simple
source_file: message_and_end.c
line: 34
project: philo
first_seen: 2025-05-07
occurrences: 2
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `message_and_end.c`
- **Ligne**: 34
- **Fonction**: ft_message
- **Projet**: philo
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
static void	error_parsing(int error)
{
	if (error == 2)
		printf("NOMBRE d'argument non valide il en faut 5 ou 6.");
	else if (error == 3)
		printf("Argument mis en parametre NULL.");
	else if (error == 4)
		printf("Echec de conversion en INT\n\
Soit: overflow | non digit | OU | valeur 0 INTERDIT pour un parametre.");
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Patterns Similaires
- [[function_philo_ae0588d6|end.c:15]] (error_parsing)
- [[function_philo_ae0588d6|end.c:15]] (error_parsing)
- [[function_philo_ae0588d6|end.c:15]] (error_parsing)
- [[function_philo_ae0588d6|end.c:15]] (error_parsing)
- [[function_philo_ae0588d6|end.c:15]] (error_parsing)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-05-07
- **Dernière mise à jour**: 2025-05-07
- **Nombre d'occurrences**: 2 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_9fb06fd5|🚚 Convoyeur de sortie (RETURN)]]
[[return_philo_df3b0f94|🚚 Convoyeur de sortie (RETURN)]]
