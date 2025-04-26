---
tags: pattern, pattern/typedef-struct, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: typedef struct
pattern_variant: simple
source_file: fdf.h
line: 55
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🔧 Typedef struct (TYPEDEF STRUCT) (Simple)

## Contexte
- **Fichier**: `fdf.h`
- **Ligne**: 55
- **Fonction**: Aucune (niveau global)
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔧 **Typedef struct**

Un pattern de type typedef struct.

## Code Source
```c
typedef struct s_data
{
	void	*img;
	char	*addr;
	int		bits_per_pixel;
	int		line_length;
	int		endian;
	void	*mlx;
	void	*mlx_win;
	t_map	*map;
	t_camera *camera;
}	t_data;
```

## Note Factorio-style
*Ce pattern fonctionne comme typedef struct dans Factorio. Il un pattern de type typedef struct.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
*Aucun pattern lié trouvé*
