---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: linux.c
line: 71
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `linux.c`
- **Ligne**: 71
- **Fonction**: I_InitMusic
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
I_InitSound
( int	samplerate,
  int	samplesize )
{

    int i;
                
    audio_fd = open("/dev/dsp", O_WRONLY);
    if (audio_fd<0)
        fprintf(stderr, "Could not open /dev/dsp\n");
         
                     
    i = 11 | (2<<16);                                           
    myioctl(audio_fd, SNDCTL_DSP_SETFRAGMENT, &i);
                    
    myioctl(audio_fd, SNDCTL_DSP_RESET, 0);
    i=11025;
    myioctl(audio_fd, SNDCTL_DSP_SPEED, &i);
    i=1;    
    myioctl(audio_fd, SNDCTL_DSP_STEREO, &i);
            
    myioctl(audio_fd, SNDCTL_DSP_GETFMTS, &i);
    if (i&=AFMT_S16_LE)    
        myioctl(audio_fd, SNDCTL_DSP_SETFMT, &i);
    else
        fprintf(stderr, "Could not play signed 16 data\n");

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
