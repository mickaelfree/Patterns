---
tags: index, pattern, factorio, project/fdf
date: 2025-04-25
project: fdf
---

# Patterns Factorio-Style pour fdf

Cette bibliothèque contient des patterns de code extraits du projet **fdf** et documentés dans un style inspiré par Factorio.
Chaque pattern est une brique logique réutilisable que vous pouvez explorer et combiner.

## Patterns par catégorie

### 🔀 Répartiteur alternatif (ELSE)

- [[else_fdf_1041c8ff|memory_manager.c:100]] my_free
- [[else_fdf_16c235a8|memory_manager.c:229]] print_memory_map

### 🔄 Chaîne de montage (FOR)

- [[for_fdf_aa045c10|memory_manager.c:129]] print_memory_content
- [[for_fdf_b3efebf6|memory_manager.c:154]] print_memory_content
- [[for_fdf_c97cbea4|memory_manager.c:159]] print_memory_content
- [[for_fdf_99e6b6b5|memory_manager.c:166]] print_memory_content
- [[for_fdf_c3c23aff|memory_manager.c:272]] main
- [[for_fdf_de035ff6|memory_manager.c:290]] main
- [[for_fdf_5b1e79d8|memory_manager.c:305]] main
- [[for_fdf_a7bc1410|memory_manager.c:322]] main

### 🏭 Usine modulaire (FUNCTION)

- [[function_fdf_7c9786dd|fdf.c:15]] parse_color
- [[function_fdf_76b4a92e|split.c:16]] ft_strlcpy
- [[function_fdf_f6d25451|memory_manager.c:19]] memory_init
- [[function_fdf_d97e0496|fdf2.c:29]] keypress
- [[function_fdf_ebfd79c9|get_next_line.c:31]] ft_find_newline
- [[function_fdf_19fe2041|fdf.c:33]] parse_color
- [[function_fdf_5db78fa6|split.c:33]] ft_strlcpy
- [[function_fdf_ce5ea355|get_next_line_utils.c:41]] ft_strlen
- [[function_fdf_463f60bb|split.c:52]] count_word
- [[function_fdf_b21f8e43|fdf2.c:53]] main
- [[function_fdf_45172d11|fdf3.c:57]] keypress
- [[function_fdf_e317deb6|get_next_line.c:58]] ft_find_newline
- [[function_fdf_5d89438a|fdf.c:65]] get_height
- [[function_fdf_af90c1ad|get_next_line.c:76]] ft_pending_save
- [[function_fdf_66af6deb|memory_manager.c:80]] my_free
- [[function_fdf_064a4270|fdf.c:87]] get_height
- [[function_fdf_3fec9e9d|memory_manager.c:106]] my_free
- [[function_fdf_e684937a|get_next_line.c:108]] main
- [[function_fdf_98eaeebf|fdf.c:113]] get_width
- [[function_fdf_0be3a958|memory_manager.c:116]] print_memory_content
- [[function_fdf_2d469bf9|fdf3.c:147]] get_height
- [[function_fdf_7ca542b5|fdf3.c:169]] get_height
- [[function_fdf_04abe544|memory_manager.c:177]] print_memory_content
- [[function_fdf_9821e8b6|fdf3.c:194]] get_width
- [[function_fdf_162b02c2|memory_manager.c:202]] inspect_allocated_block
- [[function_fdf_b8fa3833|fdf.c:212]] my_mlx_pixel_put
- [[function_fdf_9d26757f|fdf.c:223]] my_mlx_pixel_put
- [[function_fdf_a150aa9e|fdf3.c:235]] main
- [[function_fdf_dbee1e1f|memory_manager.c:246]] print_memory_state
- [[function_fdf_3618318d|fdf.c:259]] isometric
- [[function_fdf_c7a2d208|memory_manager.c:262]] print_memory_state
- [[function_fdf_5038c4c5|fdf.c:270]] isometric
- [[function_fdf_8c3a21f4|fdf.c:322]] handle_key
- [[function_fdf_ba2fa57b|fdf.c:363]] handle_key
- [[function_fdf_191f4399|fdf.c:370]] handle_close

### 🔍 Capteur logique (IF)

- [[if_fdf_36774d92|fdf.c:22]] parse_color
- [[if_fdf_dc259fa9|memory_manager.c:23]] memory_init
- [[if_fdf_b605b9fd|fdf.c:41]] ft_atoi_base
- [[if_fdf_feab5411|memory_manager.c:48]] 
- [[if_fdf_ce1a2fb3|get_next_line.c:63]] ft_pending_save
- [[if_fdf_4e629eb6|split.c:85]] 
- [[if_fdf_7431e8fd|fdf3.c:87]] 
- [[if_fdf_e585eb1f|memory_manager.c:94]] my_free
- [[if_fdf_164165a8|get_next_line.c:98]] 
- [[if_fdf_4ab363cd|split.c:106]] 
- [[if_fdf_e443114d|memory_manager.c:108]] memory_cleanup
- [[if_fdf_7439f2bb|memory_manager.c:150]] print_memory_content
- [[if_fdf_b2d910c2|fdf.c:159]] 
- [[if_fdf_beb586e6|fdf.c:165]] 
- [[if_fdf_ae7ab6ed|fdf.c:171]] 
- [[if_fdf_0d063594|memory_manager.c:179]] inspect_allocated_block
- [[if_fdf_8a459672|fdf.c:181]] 
- [[if_fdf_fd667d40|memory_manager.c:204]] print_memory_map
- [[if_fdf_9298bbd8|fdf.c:216]] my_mlx_pixel_put
- [[if_fdf_af08ab7d|memory_manager.c:227]] print_memory_map
- [[if_fdf_c3f44956|fdf.c:245]] draw_line
- [[if_fdf_e0bc6a79|fdf.c:250]] draw_line
- [[if_fdf_0090e3b9|fdf.c:304]] 
- [[if_fdf_093acad7|fdf.c:310]] 
- [[if_fdf_dc9b738d|fdf.c:324]] handle_key
- [[if_fdf_8cb21d89|fdf.c:375]] main
- [[if_fdf_178e2e27|fdf.c:382]] main

### 🚚 Convoyeur de sortie (RETURN)

- [[return_fdf_9fb06fd5|get_next_line_utils.c:17]] 
- [[return_fdf_5f6fc41e|get_next_line.c:25]] 
- [[return_fdf_d183ade1|split.c:26]] ft_strlcpy
- [[return_fdf_df45ddab|get_next_line.c:28]] 
- [[return_fdf_2a890ee3|fdf.c:30]] parse_color
- [[return_fdf_d183ade1|split.c:31]] ft_strlcpy
- [[return_fdf_650ccd10|fdf2.c:33]] keypress
- [[return_fdf_df45ddab|get_next_line_utils.c:38]] 
- [[return_fdf_18984f02|get_next_line.c:39]] ft_find_newline
- [[return_fdf_b80353c7|get_next_line.c:41]] ft_find_newline
- [[return_fdf_18984f02|get_next_line.c:43]] ft_find_newline
- [[return_fdf_9dc37e69|get_next_line.c:45]] ft_find_newline
- [[return_fdf_b83d5c36|get_next_line_utils.c:46]] ft_strlen
- [[return_fdf_18984f02|get_next_line.c:47]] ft_find_newline
- [[return_fdf_59960867|split.c:49]] count_word
- [[return_fdf_a98cfb70|get_next_line.c:49]] ft_find_newline
- [[return_fdf_72b084d1|fdf2.c:50]] 
- [[return_fdf_18984f02|get_next_line.c:51]] ft_find_newline
- [[return_fdf_b80353c7|get_next_line_utils.c:51]] ft_strlen
- [[return_fdf_55949d95|get_next_line.c:53]] ft_find_newline
- [[return_fdf_9dc37e69|get_next_line_utils.c:53]] ft_strlen
- [[return_fdf_a98cfb70|get_next_line_utils.c:55]] ft_strlen
- [[return_fdf_55949d95|get_next_line_utils.c:57]] ft_strlen
- [[return_fdf_3fed850e|fdf.c:61]] ft_atoi_base
- [[return_fdf_650ccd10|fdf3.c:62]] keypress
- [[return_fdf_9fb06fd5|split.c:70]] 
- [[return_fdf_b83d5c36|fdf.c:73]] get_height
- [[return_fdf_9fb06fd5|split.c:73]] 
- [[return_fdf_7e82b804|split.c:74]] 
- [[return_fdf_fb179552|memory_manager.c:77]] 
- [[return_fdf_7aa30fec|fdf3.c:81]] 
- [[return_fdf_63aaece2|fdf.c:84]] get_height
- [[return_fdf_9fb06fd5|split.c:88]] 
- [[return_fdf_7e82b804|split.c:91]] 
- [[return_fdf_b83d5c36|fdf.c:96]] get_width
- [[return_fdf_feb12e11|get_next_line.c:97]] 
- [[return_fdf_b83d5c36|fdf.c:99]] get_width
- [[return_fdf_9fb06fd5|split.c:102]] 
- [[return_fdf_a14f8516|get_next_line.c:105]] 
- [[return_fdf_e46a9617|fdf.c:110]] get_width
- [[return_fdf_9fb06fd5|split.c:113]] 
- [[return_fdf_f830ac5d|get_next_line.c:115]] main
- [[return_fdf_7aa30fec|fdf3.c:119]] 
- [[return_fdf_7e82b804|split.c:120]] 
- [[return_fdf_b83d5c36|get_next_line.c:122]] main
- [[return_fdf_9fb06fd5|fdf.c:132]] 
- [[return_fdf_a14f8516|fdf.c:142]] 
- [[return_fdf_b83d5c36|fdf3.c:155]] get_height
- [[return_fdf_9fb06fd5|fdf.c:156]] 
- [[return_fdf_9fb06fd5|fdf.c:162]] 
- [[return_fdf_63aaece2|fdf3.c:167]] get_height
- [[return_fdf_9fb06fd5|fdf.c:168]] 
- [[return_fdf_9fb06fd5|fdf.c:175]] 
- [[return_fdf_b83d5c36|fdf3.c:178]] get_width
- [[return_fdf_b83d5c36|fdf3.c:181]] get_width
- [[return_fdf_9fb06fd5|fdf.c:188]] 
- [[return_fdf_799418d9|fdf3.c:191]] get_width
- [[return_fdf_51af0abe|fdf.c:208]] 
- [[return_fdf_72b084d1|fdf3.c:232]] 
- [[return_fdf_804c07ca|fdf.c:286]] project_point
- [[return_fdf_650ccd10|memory_manager.c:336]] main
- [[return_fdf_b83d5c36|fdf.c:360]] handle_key
- [[return_fdf_b83d5c36|fdf.c:367]] handle_close
- [[return_fdf_f830ac5d|fdf.c:378]] main
- [[return_fdf_f830ac5d|fdf.c:385]] main
- [[return_fdf_b83d5c36|fdf.c:410]] main

### 📐 Plan d'assemblage (STRUCT)

- [[struct_fdf_c86e0c41|memory_manager.c:8]] 
- [[struct_fdf_ee61ae0a|fdf2.c:21]] 
- [[struct_fdf_92a74403|fdf.h:29]] 
- [[struct_fdf_ee61ae0a|fdf3.c:32]] 
- [[struct_fdf_5f8f2e89|fdf.h:37]] 
- [[struct_fdf_23522a89|fdf3.c:41]] 
- [[struct_fdf_8d512dcc|fdf.h:44]] 
- [[struct_fdf_ef880ab7|fdf3.c:50]] 
- [[struct_fdf_2ae07bf5|fdf.h:55]] 

### 🔧 Typedef struct (TYPEDEF STRUCT)

- [[typedef_struct_fdf_9dd1b67c|memory_manager.c:8]] 
- [[typedef_struct_fdf_e0cd2fb6|fdf2.c:21]] 
- [[typedef_struct_fdf_c449ceb7|fdf.h:29]] 
- [[typedef_struct_fdf_e0cd2fb6|fdf3.c:32]] 
- [[typedef_struct_fdf_7e9f39fa|fdf.h:37]] 
- [[typedef_struct_fdf_f5e83c04|fdf3.c:41]] 
- [[typedef_struct_fdf_28133740|fdf.h:44]] 
- [[typedef_struct_fdf_22933af6|fdf3.c:50]] 
- [[typedef_struct_fdf_2edf9462|fdf.h:55]] 

### ⭕ Tapis roulant surveillé (WHILE)

- [[while_fdf_fd5a0011|get_next_line_utils.c:27]] 
- [[while_fdf_b27ffe22|get_next_line_utils.c:32]] 
- [[while_fdf_5e9c0ba5|get_next_line.c:36]] ft_find_newline
- [[while_fdf_72b81cb5|split.c:40]] count_word
- [[while_fdf_97f84fa7|fdf.c:46]] ft_atoi_base
- [[while_fdf_dbc35aae|memory_manager.c:47]] 
- [[while_fdf_4be7f7d8|get_next_line_utils.c:48]] ft_strlen
- [[while_fdf_47fb3716|split.c:57]] free_tab
- [[while_fdf_65b2c704|get_next_line.c:66]] ft_pending_save
- [[while_fdf_694d9f90|fdf.c:75]] get_height
- [[while_fdf_af2b734b|fdf3.c:82]] 
- [[while_fdf_c00fea89|get_next_line.c:92]] 
- [[while_fdf_0192158f|memory_manager.c:93]] my_free
- [[while_fdf_3f9e0e2f|split.c:104]] 
- [[while_fdf_36c5c3f6|get_next_line.c:116]] main
- [[while_fdf_c30b7456|fdf3.c:120]] 
- [[while_fdf_fe027d1d|fdf3.c:133]] 
- [[while_fdf_694d9f90|fdf3.c:157]] get_height
- [[while_fdf_7ee61420|fdf.c:178]] 
- [[while_fdf_37e61a91|fdf3.c:184]] get_width
- [[while_fdf_0d6369dc|fdf3.c:198]] init_grid
- [[while_fdf_009fd49f|memory_manager.c:218]] print_memory_map
- [[while_fdf_02d686e8|fdf.c:239]] draw_line
- [[while_fdf_c6b2ac6e|memory_manager.c:251]] print_memory_state
- [[while_fdf_1e9fb3cb|fdf.c:297]] 


## Statistiques

- **Total de patterns extraits**: 181
- **Types de patterns**: 8
- **Date de génération**: 2025-04-25 16:59:09

## Retour à l'index général
[[index|Retour à l'index général des patterns]]

## Graphe de patterns

Pour visualiser les connexions entre les patterns de ce projet, ouvrez la [Vue graphique](obsidian://graph) dans Obsidian 
et filtrez par le tag `project/fdf`.
