---
tags: pattern, pattern/function, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: function
pattern_variant: simple
source_file: i_sound.c
line: 737
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: non
---

# 🏭 Usine modulaire (FUNCTION) (Simple)

## Contexte
- **Fichier**: `i_sound.c`
- **Ligne**: 737
- **Fonction**: I_ShutdownSound
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🏭 **Usine modulaire**

Comme une usine qui prend des entrées, effectue un traitement, et produit des sorties.

## Code Source
```c
void
I_InitSound()
{ 
#ifdef SNDSERV
  char buffer[256];
  
  if (getenv("DOOMWADDIR"))
    sprintf(buffer, "%s/%s",
	    getenv("DOOMWADDIR"),
	    sndserver_filename);
  else
    sprintf(buffer, "%s", sndserver_filename);
  
  // start sound process
  if ( !access(buffer, X_OK) )
  {
    strcat(buffer, " -quiet");
    sndserver = popen(buffer, "w");
  }
  else
    fprintf(stderr, "Could not start sound server [%s]\n", buffer);
#else
    
  int i;
  
#ifdef SNDINTR
  fprintf( stderr, "I_SoundSetTimer: %d microsecs\n", SOUND_INTERVAL );
  I_SoundSetTimer( SOUND_INTERVAL );
#endif
    
  // Secure and configure sound device first.
  fprintf( stderr, "I_InitSound: ");
  
  audio_fd = open("/dev/dsp", O_WRONLY);
  if (audio_fd<0)
    fprintf(stderr, "Could not open /dev/dsp\n");
  
                     
  i = 11 | (2<<16);                                           
  myioctl(audio_fd, SNDCTL_DSP_SETFRAGMENT, &i);
  myioctl(audio_fd, SNDCTL_DSP_RESET, 0);
  
  i=SAMPLERATE;
  
  myioctl(audio_fd, SNDCTL_DSP_SPEED, &i);
  
  i=1;
  myioctl(audio_fd, SNDCTL_DSP_STEREO, &i);
  
  myioctl(audio_fd, SNDCTL_DSP_GETFMTS, &i);
  
  if (i&=AFMT_S16_LE)    
    myioctl(audio_fd, SNDCTL_DSP_SETFMT, &i);
  else
    fprintf(stderr, "Could not play signed 16 data\n");

  fprintf(stderr, " configured audio device\n" );

    
  // Initialize external data (all sounds) at start, keep static.
  fprintf( stderr, "I_InitSound: ");
  
  for (i=1 ; i<NUMSFX ; i++)
  { 
    // Alias? Example is the chaingun sound linked to pistol.
    if (!S_sfx[i].link)
    {
      // Load data from WAD file.
      S_sfx[i].data = getsfx( S_sfx[i].name, &lengths[i] );
    }	
    else
    {
      // Previously loaded already?
      S_sfx[i].data = S_sfx[i].link->data;
      lengths[i] = lengths[(S_sfx[i].link - S_sfx)/sizeof(sfxinfo_t)];
    }
  }

  fprintf( stderr, " pre-cached all sound data\n");
  
  // Now initialize mixbuffer with zero.
  for ( i = 0; i< MIXBUFFERSIZE; i++ )
    mixbuffer[i] = 0;
  
  // Finished initialization.
  fprintf(stderr, "I_InitSound: sound module ready\n");
    
#endif
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
