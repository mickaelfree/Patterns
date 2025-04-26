---
tags: pattern, pattern/if, factorio, code-logic, project/DOOM, pattern/variant/nested
date: 2025-04-25
pattern_type: if
pattern_variant: nested
source_file: m_menu.c
line: 1519
project: DOOM
first_seen: 2025-04-25
occurrences: 1
ai_analyzed: non
optimizable: oui
---

# 🔍 Capteur logique (IF) (Capteur en cascade)

## Contexte
- **Fichier**: `m_menu.c`
- **Ligne**: 1519
- **Fonction**: Aucune (niveau global)
- **Projet**: DOOM
- **Variante**: Capteur en cascade
- **Complexité**: élevée

## Métaphore Factorio
🔍 **Capteur logique**

Comme un capteur dans Factorio qui active un circuit uniquement lorsqu'une condition est remplie.

## Code Source
```c
if (!menuactive)
	switch(ch)
	{
	  case KEY_MINUS:         // Screen size down
	    if (automapactive || chat_on)
		return false;
	    M_SizeDisplay(0);
	    S_StartSound(NULL,sfx_stnmov);
	    return true;
				
	  case KEY_EQUALS:        // Screen size up
	    if (automapactive || chat_on)
		return false;
	    M_SizeDisplay(1);
	    S_StartSound(NULL,sfx_stnmov);
	    return true;
				
	  case KEY_F1:            // Help key
	    M_StartControlPanel ();

	    if ( gamemode == retail )
	      currentMenu = &ReadDef2;
	    else
	      currentMenu = &ReadDef1;
	    
	    itemOn = 0;
	    S_StartSound(NULL,sfx_swtchn);
	    return true;
				
	  case KEY_F2:            // Save
	    M_StartControlPanel();
	    S_StartSound(NULL,sfx_swtchn);
	    M_SaveGame(0);
	    return true;
				
	  case KEY_F3:            // Load
	    M_StartControlPanel();
	    S_StartSound(NULL,sfx_swtchn);
	    M_LoadGame(0);
	    return true;
				
	  case KEY_F4:            // Sound Volume
	    M_StartControlPanel ();
	    currentMenu = &SoundDef;
	    itemOn = sfx_vol;
	    S_StartSound(NULL,sfx_swtchn);
	    return true;
				
	  case KEY_F5:            // Detail toggle
	    M_ChangeDetail(0);
	    S_StartSound(NULL,sfx_swtchn);
	    return true;
				
	  case KEY_F6:            // Quicksave
	    S_StartSound(NULL,sfx_swtchn);
	    M_QuickSave();
	    return true;
				
	  case KEY_F7:            // End game
	    S_StartSound(NULL,sfx_swtchn);
	    M_EndGame(0);
	    return true;
				
	  case KEY_F8:            // Toggle messages
	    M_ChangeMessages(0);
	    S_StartSound(NULL,sfx_swtchn);
	    return true;
				
	  case KEY_F9:            // Quickload
	    S_StartSound(NULL,sfx_swtchn);
	    M_QuickLoad();
	    return true;
				
	  case KEY_F10:           // Quit DOOM
	    S_StartSound(NULL,sfx_swtchn);
	    M_QuitDOOM(0);
	    return true;
				
	  case KEY_F11:           // gamma toggle
	    usegamma++;
	    if (usegamma > 4)
		usegamma = 0;
	    players[consoleplayer].message = gammamsg[usegamma];
	    I_SetPalette (W_CacheLumpName ("PLAYPAL",PU_CACHE));
	    return true;
				
	}
```

## Analyse Structurelle
**Type détecté**: Capteur en cascade

Ces capteurs en cascade pourraient être combinés en un seul réseau logique avec des opérateurs && ou ||.

**Analogie Factorio**:
Comme plusieurs capteurs en série dans Factorio que vous pourriez remplacer par un circuit combinatoire unique.

## Note Factorio-style
*Ce pattern fonctionne comme capteur logique dans Factorio. Il comme un capteur dans factorio qui active un circuit uniquement lorsqu'une condition est remplie.*

## Patterns Similaires
- [[if_DOOM_c0802a70|p_switch.c:284]] (P_UseSpecialLine)
- [[if_DOOM_d2a150dd|p_setup.c:318]] (if)

## Note Perso
*Ajouter vos notes personnelles ici...*

## Statistiques du Pattern
- **Première détection**: 2025-04-25
- **Dernière mise à jour**: 2025-04-25
- **Nombre d'occurrences**: 1 fichiers
- **Analysé par IA**: Non
- **Optimisable**: Oui

## Patterns liés
[[else_DOOM_15ea13cc|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_0faf1aab|🔀 Répartiteur alternatif (ELSE)]]
[[else_DOOM_29abfc46|🔀 Répartiteur alternatif (ELSE)]]
[[else_if_DOOM_9dbf5077|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_88acfb35|🔄 Répartiteur intelligent (ELSE IF)]]
[[else_if_DOOM_59fd791e|🔄 Répartiteur intelligent (ELSE IF)]]
[[switch_DOOM_83fe174e|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_17419957|🔀 Aiguillage multiple (SWITCH)]]
[[switch_DOOM_b47d2988|🔀 Aiguillage multiple (SWITCH)]]
