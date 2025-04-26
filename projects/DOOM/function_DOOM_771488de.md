---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: soundsrv.c
line: 537
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `soundsrv.c`
- **Ligne**: 537
- **Fonction**: outputushort
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void initdata(void)
{

    int		i;
    int		j;
    
    int*	steptablemid = steptable + 128;

    for (i=0 ;
	 i<sizeof(channels)/sizeof(unsigned char *) ;
	 i++)
    {
	channels[i] = 0;
    }
    
    gettimeofday(&last, &whocares);

    for (i=-128 ; i<128 ; i++)
	steptablemid[i] = pow(2.0, (i/64.0))*65536.0;

    // generates volume lookup tables
    //  which also turn the unsigned samples
    //  into signed samples
    // for (i=0 ; i<128 ; i++)
    // for (j=0 ; j<256 ; j++)
    // vol_lookup[i*256+j] = (i*(j-128))/127;
    
    for (i=0 ; i<128 ; i++)
	for (j=0 ; j<256 ; j++)
	    vol_lookup[i*256+j] = (i*(j-128)*256)/127;

}
```

## Note Factorio-style
*Ce pattern fonctionne comme usine modulaire dans Factorio. Il comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.*

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Non

## Patterns liés
[[return_DOOM_3e1b4f0f|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
[[return_DOOM_e198b61b|🚚 Convoyeur de sortie (RETURN)]]
