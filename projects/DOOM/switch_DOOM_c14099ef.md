---
tags: pattern, pattern/switch, factorio, code-logic, project/DOOM, pattern/variant/simple
date: 2025-04-25
pattern_type: switch
pattern_variant: simple
source_file: soundsrv.c
line: 653
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔀 Aiguillage multiple (SWITCH) (Simple)

## Contexte
- **Fichier**: `soundsrv.c`
- **Ligne**: 653
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Simple
- **Complexité**: standard

## Métaphore Factorio
🔀 **Aiguillage multiple**

Comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.

## Code Source
```c
switch (commandbuf[0])
			{
			  case 'p':
			    // play a new sound effect
			    read(0, commandbuf, 9);

			    if (snd_verbose)
			    {
				commandbuf[9]=0;
				fprintf(stderr, "%s\n", commandbuf);
			    }

			    commandbuf[0] -=
				commandbuf[0]>='a' ? 'a'-10 : '0';
			    commandbuf[1] -=
				commandbuf[1]>='a' ? 'a'-10 : '0';
			    commandbuf[2] -=
				commandbuf[2]>='a' ? 'a'-10 : '0';
			    commandbuf[3] -=
				commandbuf[3]>='a' ? 'a'-10 : '0';
			    commandbuf[4] -=
				commandbuf[4]>='a' ? 'a'-10 : '0';
			    commandbuf[5] -=
				commandbuf[5]>='a' ? 'a'-10 : '0';
			    commandbuf[6] -=
				commandbuf[6]>='a' ? 'a'-10 : '0';
			    commandbuf[7] -=
				commandbuf[7]>='a' ? 'a'-10 : '0';

			    //	p<snd#><step><vol><sep>
			    sndnum = (commandbuf[0]<<4) + commandbuf[1];
			    step = (commandbuf[2]<<4) + commandbuf[3];
			    step = steptable[step];
			    vol = (commandbuf[4]<<4) + commandbuf[5];
			    sep = (commandbuf[6]<<4) + commandbuf[7];

			    handle = addsfx(sndnum, vol, step, sep);
			    // returns the handle
			    //	outputushort(handle);
			    break;
			    
			  case 'q':
			    read(0, commandbuf, 1);
			    waitingtofinish = 1; rc = 0;
			    break;
			    
			  case 's':
			  {
			      int fd;
			      read(0, commandbuf, 3);
			      commandbuf[2] = 0;
			      fd = open((char*)commandbuf, O_CREAT|O_WRONLY, 0644);
			      commandbuf[0] -= commandbuf[0]>='a' ? 'a'-10 : '0';
			      commandbuf[1] -= commandbuf[1]>='a' ? 'a'-10 : '0';
			      sndnum = (commandbuf[0]<<4) + commandbuf[1];
			      write(fd, S_sfx[sndnum].data, lengths[sndnum]);
			      close(fd);
			  }
			  break;
			  
			  default:
			    fprintf(stderr, "Did not recognize command\n");
			    break;
			}
```

## Analyse Structurelle
**Type détecté**: Simple

Cet aiguillage ne gère que 0 voies - un simple if/else serait plus efficace.

**Analogie Factorio**:
Comme un réseau ferroviaire complexe pour seulement 2 destinations - un simple répartiteur suffirait.

## Note Factorio-style
*Ce pattern fonctionne comme aiguillage multiple dans Factorio. Il comme un aiguillage ferroviaire qui dirige vers différentes voies selon la valeur évaluée.*

## Patterns Similaires
- [[switch_DOOM_c17ea736|p_floor.c:64]] (switch)
- [[switch_DOOM_a6dcfac8|p_floor.c:131]] (switch)
- [[switch_DOOM_06435d32|p_spec.c:1020]] (P_PlayerInSpecialSector)
- [[switch_DOOM_8b4f7b34|p_spec.c:1276]] (P_SpawnSpecials)
- [[switch_DOOM_b4134f01|p_lights.c:316]] (T_Glow)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[if_DOOM_243776b2|🔍 Capteur logique (IF)]]
[[if_DOOM_e95e8e34|🔍 Capteur logique (IF)]]
[[if_DOOM_e74900f0|🔍 Capteur logique (IF)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
