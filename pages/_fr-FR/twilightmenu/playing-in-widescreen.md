---
lang: fr-FR
layout: wiki
section: twilightmenu
category: other
title: Jouer en plein écran
description: How to use TWiLight Menu++ in widescreen on the Nintendo 3DS
---

Nécessite une Old/New Nintendo 3DS ou 2DS.

**Préparation**
- Assurez-vous que le `boot.firm` de Luma est à la racine de la carte SD pour que cela fonctionne
- Si vous avez utilisé TWiLight Menu++ Updater ou Universal-Updater pour mettre à jour, veuillez installer la dernière CIA de TWiLight Menu++ en utilisant FBI

1. Download [TWPatch](https://sono.9net.org/hebrew/TWPatch/data/TWPatch.cia) ([GBATemp thread](https://gbatemp.net/threads/twpatcher-ds-i-mode-screen-filters-and-patches.542694/))
1. Dans la configuration de Luma, activez "enable external FIRMs and modules"
1. Install the TWPatch CIA
1. Launch TWPatch
1. (Optional!) For a less pixelated widescreen, hold Y+B, and enable `GPU scale test (health hazard!)`
1. Press <kbd class="face">X</kbd> + <kbd>START</kbd> to generate a `TwlBg.cxi` file with widescreen
   - If the top screen doesn't indicate that wide patch is enabled, start from step 4 again
   - If widescreen still doesn't work, wait for RTCom-activated widescreen to be released
1. In the TWiLight Menu++ settings, switch the page to `Misc settings`, and set `Screen Aspect Ratio` to `16:10`
   - This can be done per-game as well

You're all done! Enjoy your DS games in widescreen!

**NOTE1**: Every game/app in DS(i) mode will run in widescreen, even the games that aren't compatible with widescreen. For this to be fixed so only the widescreen-compatible games run in widescreen, wait for RTCom-activated widescreen to be released.

**NOTE2:** Do not hold <kbd>START</kbd> or <kbd>SELECT</kbd> when launching TWLMenu++, if you don't want widescreen to look glitched. If you don't see the screen aspect ratio setting, wait for RTCom-activated widescreen to be released.

Not every game is widescreen compatible. [We have created a list of games with widescreen](https://github.com/DS-Homebrew/TWiLightMenu/blob/master/7zfile/3DS%20-%20CFW%20users/Games%20supported%20with%20widescreen.txt)
