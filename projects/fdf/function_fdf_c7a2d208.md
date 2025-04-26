---
tags: pattern, pattern/function, factorio, code-logic, project/fdf, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: memory_manager.c
line: 262
project: fdf
first_seen: 2025-04-25
occurrences: 6
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `memory_manager.c`
- **Ligne**: 262
- **Fonction**: print_memory_state
- **Projet**: fdf
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
Programme de test
int main() {
    printf("Initialisation du gestionnaire de mémoire...\n");
    memory_init();
    print_memory_map();
    
    printf("Test 1: Allocation d'un tableau d'entiers\n");
    int *array = (int*)my_malloc(10 * sizeof(int));
    
    // Initialisation du tableau
    for (int i = 0; i < 10; i++) {
        array[i] = i * 100;
    }
    
    print_memory_map();
    inspect_allocated_block(array, 40); // Afficher les 40 premiers octets
    
    printf("\nTest 2: Allocation d'une chaîne de caractères\n");
    char *message = (char*)my_malloc(20);
    strcpy(message, "Bonjour monde!");
    
    print_memory_map();
    inspect_allocated_block(message, 20); // Afficher les 20 premiers octets
    
    printf("\nTest 3: Allocation d'un tableau de double\n");
    double *values = (double*)my_malloc(5 * sizeof(double));
    
    // Initialisation des valeurs
    for (int i = 0; i < 5; i++) {
        values[i] = 3.14159 * (i + 1);
    }
    
    print_memory_map();
    inspect_allocated_block(values, 40); // Afficher les 40 premiers octets
    
    printf("\nTest 4: Libération du premier bloc\n");
    my_free(array);
    print_memory_map();
    
    printf("Test 5: Réallocation dans l'espace libéré\n");
    float *new_array = (float*)my_malloc(8 * sizeof(float));
    
    // Initialisation du nouveau tableau
    for (int i = 0; i < 8; i++) {
        new_array[i] = (float)i * 1.5f;
    }
    
    print_memory_map();
    inspect_allocated_block(new_array, 32); // Afficher les 32 premiers octets
    
    printf("\nTest 6: Libération de tous les blocs pour tester la fusion\n");
    my_free(message);
    my_free(values);
    my_free(new_array);
    print_memory_map();
    
    printf("Test 7: Allocation d'un gros bloc\n");
    char *big_block = (char*)my_malloc(1024);
    
    // Remplir le bloc avec un motif
    for (int i = 0; i < 1024; i++) {
        big_block[i] = i % 26 + 'A';
    }
    
    print_memory_map();
    inspect_allocated_block(big_block, 64); // Afficher les 64 premiers octets
    
    printf("\nTest 8: Nettoyage final\n");
    my_free(big_block);
    print_memory_map();
    
    memory_cleanup();
    printf("Mémoire libérée, test terminé.\n");
    
    return 0;
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
