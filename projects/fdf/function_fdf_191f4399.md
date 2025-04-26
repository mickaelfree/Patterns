---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: fdf.c
line: 370
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `fdf.c`
- **Ligne**: 370
- **Fonction**: handle_close
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
int	main(int argc, char **argv)
{
	t_data		img;
	t_camera	camera;
	
	if (argc != 2)
	{
		ft_putstr_fd("Usage: ./fdf <filename.fdf>\n", 1);
		return (1);
	}
	
	img.map = parse_map(argv[1]);
	if (!img.map)
	{
		ft_putstr_fd("Error: invalid map file\n", 1);
		return (1);
	}
	
	camera.zoom = 20;
	camera.alpha = 0.8;
	camera.beta = 0.8;
	camera.gamma = 0;
	camera.x_offset = WIDTH / 2;
	camera.y_offset = HEIGHT / 3;
	camera.projection = 1;
	img.camera = &camera;
	
	img.mlx = mlx_init();
	img.mlx_win = mlx_new_window(img.mlx, WIDTH, HEIGHT, "FDF - Wireframe Renderer");
	img.img = mlx_new_image(img.mlx, WIDTH, HEIGHT);
	img.addr = mlx_get_data_addr(img.img, &img.bits_per_pixel, 
		&img.line_length, &img.endian);
	
	draw_map(&img);
	mlx_put_image_to_window(img.mlx, img.mlx_win, img.img, 0, 0);
	
	mlx_key_hook(img.mlx_win, handle_key, &img);
	mlx_hook(img.mlx_win, 17, 0, handle_close, &img);
	mlx_loop(img.mlx);
	
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
