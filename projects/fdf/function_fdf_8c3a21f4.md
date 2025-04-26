---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: fdf.c
line: 322
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 322
- **Fonction**: handle_key
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	handle_key(int keycode, t_data *data)
{
	if (keycode == XK_Escape)
	{
		mlx_destroy_window(data->mlx, data->mlx_win);
		exit(0);
	}
	else if (keycode == XK_equal || keycode == XK_plus)
		data->camera->zoom += 1;
	else if (keycode == XK_minus && data->camera->zoom > 1)
		data->camera->zoom -= 1;
	else if (keycode == XK_Up)
		data->camera->y_offset -= 10;
	else if (keycode == XK_Down)
		data->camera->y_offset += 10;
	else if (keycode == XK_Left)
		data->camera->x_offset -= 10;
	else if (keycode == XK_Right)
		data->camera->x_offset += 10;
	else if (keycode == XK_a)
		data->camera->alpha += 0.1;
	else if (keycode == XK_d)
		data->camera->alpha -= 0.1;
	else if (keycode == XK_w)
		data->camera->beta += 0.1;
	else if (keycode == XK_s)
		data->camera->beta -= 0.1;
	else if (keycode == XK_space)
		data->camera->projection = !data->camera->projection;
	
	mlx_clear_window(data->mlx, data->mlx_win);
	mlx_destroy_image(data->mlx, data->img);
	data->img = mlx_new_image(data->mlx, WIDTH, HEIGHT);
	data->addr = mlx_get_data_addr(data->img, &data->bits_per_pixel, 
		&data->line_length, &data->endian);
	draw_map(data);
	mlx_put_image_to_window(data->mlx, data->mlx_win, data->img, 0, 0);
	
	return (0);
}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 6 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_fdf_2a890ee3|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_3fed850e|🚚 Convoyeur de sortie (RETURN)]]
[[return_fdf_b83d5c36|🚚 Convoyeur de sortie (RETURN)]]
