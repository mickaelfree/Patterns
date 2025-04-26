---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: soundsrv.c
line: 512
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `soundsrv.c`
- **Ligne**: 512
- **Fonction**: outputushort
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void outputushort(int num)
{

    static unsigned char	buff[5] = { 0, 0, 0, 0, '\n' };
    static char*		badbuff = "xxxx\n";

    // outputs a 16-bit # in hex or "xxxx" if -1.
    if (num < 0)
    {
	write(1, badbuff, 5);
    }
    else
    {
	buff[0] = num>>12;
	buff[0] += buff[0] > 9 ? 'a'-10 : '0';
	buff[1] = (num>>8) & 0xf;
	buff[1] += buff[1] > 9 ? 'a'-10 : '0';
	buff[2] = (num>>4) & 0xf;
	buff[2] += buff[2] > 9 ? 'a'-10 : '0';
	buff[3] = num & 0xf;
	buff[3] += buff[3] > 9 ? 'a'-10 : '0';
	write(1, buff, 5);
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
