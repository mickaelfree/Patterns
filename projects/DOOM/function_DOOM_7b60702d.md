---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: wadread.c
line: 152
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `wadread.c`
- **Ligne**: 152
- **Fonction**: filelength
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void openwad(char* wadname)
{

    int		wadfile;
    int		tableoffset;
    int		tablelength;
    int		tablefilelength;
    int		i;
    wadinfo_t	header;
    filelump_t*	filetable;

    // open and read the wadfile header
    wadfile = open(wadname, O_RDONLY);

    if (wadfile < 0)
	derror("Could not open wadfile");

    read(wadfile, &header, sizeof header);

    if (strncmp(header.identification, "IWAD", 4))
	derror("wadfile has weirdo header");

    numlumps = LONG(header.numlumps);
    tableoffset = LONG(header.infotableofs);
    tablelength = numlumps * sizeof(lumpinfo_t);
    tablefilelength = numlumps * sizeof(filelump_t);
    lumpinfo = (lumpinfo_t *) malloc(tablelength);
    filetable = (filelump_t *) ((char*)lumpinfo + tablelength - tablefilelength);

    // get the lumpinfo table
    lseek(wadfile, tableoffset, SEEK_SET);
    read(wadfile, filetable, tablefilelength);

    // process the table to make the endianness right and shift it down
    for (i=0 ; i<numlumps ; i++)
    {
	strncpy(lumpinfo[i].name, filetable[i].name, 8);
	lumpinfo[i].handle = wadfile;
	lumpinfo[i].filepos = LONG(filetable[i].filepos);
	lumpinfo[i].size = LONG(filetable[i].size);
	// fprintf(stderr, "lump [%.8s] exists\n", lumpinfo[i].name);
    }

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
