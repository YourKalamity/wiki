---
lang: it-IT
layout: wiki
section: ds-index
category: guides
title: Scorciatoie giochi del DS (3DS)
description: Come creare scorciatoie CIA per avere i tuoi giochi DS nel menu home del tuo 3DS
---

Se hai qualche problema, controlla le FAQ sul thread [GBAtemp](https://gbatemp.net/threads/nds-forwarder-cias-for-your-home-menu.426174/).
{:.alert .alert-warning}

### Requisiti

3DS:
- [Luma3DS](https://github.com/lumateam/luma3ds/releases), o qualsiasi altro CFW che patcha TWL_NAND
- [FBI](https://github.com/Steveice10/FBI/releases) per installare i file CIA
- (Facoltativa) Una flashcard DS supportata

{% capture flashcards %}
Le flashcard raccomandate sono DSTT e Acekard 2i. Se vuoi una perfetta compatibilità con i giochi, prendi la SuperCard DSTWO / DSTWO PLUS. L'unico svantaggio è che svuota la batteria del sistema più velocemente.

Se hai una flashcard che funziona con il Launcher NTR di Apache Thunder, non esitare a richiederla [sul thread GBAtemp](https://gbatemp.net/threads/nds-forwarder-cias-for-your-home-menu.426174/). Assicurati di specificare quale build stai usando (Normale o Alt), e se `RESETSLOT1` è impostato a `0` o `1` in `sd:/nds/ntr_launcher. ni`.

Compatibile:
- [Acekard 2(i)](http://www.nds-card.com/ProShow.asp?ProID=160) (i giochi DSi-Enhanced, compresi i giochi più recenti NTR, non funzionano.)
- [Acekard RPG](http://wiki.gbatemp.net/wiki/Acekard_RPG)
- [DSTT](http://www.nds-card.com/ProShow.asp?ProID=157)
- [DSTT Advance](http://kaze-tado.way-nifty.com/moo/images/2008/11/19/200811202.jpg)
- Galaxy Eagle
- M3 DS Real
- [M3 DS Simply](https://farm2.static.flickr.com/1333/752793411_d91b182eb7.jpg) (utilizza  una <scheda microSD da 2GB)
- [R4 DS](http://www.nds-card.com/ProShow.asp?ProID=141) (versione originale non-SDHC, utilizza una <scheda microSD da 2GB)
- [R4 SDHC Snoopy](http://www.nds-card.com/ProShow.asp?ProID=567)
- [R4 SDHC RTS LITE](http://www.nds-card.com/ProShow.asp?ProID=450) ([www.r4isdhc.com](http://www.r4isdhc.com/))
- R4 SDHC Upgrade ([www.r4i-sdhc.com](http://www.r4i-sdhc.com/))
- [R4i3D](http://www.3ds-cart.com/en/other-flashcarts/35-r4i3d-revolution-cart-for-3ds-dsi-dsl-ds.html) ([www.r4i3d.com](http://www.r4i-sdhc.com/))
- [R4iDSN](http://3ds-flashcard.com/home/28-r4idsn-3ds.html)
- [R4i Gold](http://www.nds-card.com/ProShow.asp?ProID=330)
- [R4i Gold RTS](http://www.nds-card.com/ProShow.asp?ProID=149) ([www.r4ids.cn](http://www.r4ids.cn/))
- [R4i-SDHC](http://www.nds-card.com/ProShow.asp?ProID=146) ([www.r4i-sdhc.com](http://www.r4i-sdhc.com)) (Versione Normale e RTS)
- R4iTT ([www.r4itt.net](http://www.r4itt.net/)) (La Purple card potrebbe essere incompatible)
- [SuperCard DSONE](http://wiki.gbatemp.net/wiki/SuperCard_DSONEi)
- [SuperCard DSTWO](http://www.nds-card.com/ProShow.asp?ProID=135) (versioni Normale e Plus)

Non Testato:
- R4i3D NUOVO (utilizza modello e pacchetto R4iDSN)

Parzialmente compatibile:
- Ace 3DS+ (compatibilità con i giochi pessima, quindi il salvataggio/caricamento dei file di salvataggio risulta in un crash.)
- Gateway Blue Card (compatibilità con i giochi pessima, quindi il salvataggio/caricamento dei file di salvataggio risulta in un crash.)
- EX4DS (compatibilità con i giochi pessima, quindi il salvataggio/caricamento dei file di salvataggio risulta in un crash.)
- R4iLS (compatibilità con i giochi pessima, quindi il salvataggio/caricamento dei file di salvataggio risulta in un crash.)
- Le flashcard con [www.r4isdhc.com.cn](http://www.r4isdhc.com.cn/) (La compatibilità con i giochi è pessima, quindi il salvataggio/caricamento dei file risulta in crash.)

Incompatibile:
- CycloDS (i)Evolution (Può auto-avviare le ROM, ma funziona in modo diverso rispetto ad altre flashcard.)
- (i)Edge (Impossibile effettuare l'autoboot di una .nds ROM)
- R4 Gold Pro ([www.r4i-gold.com](http://www.r4i-gold.com)/[www.r4i-gold.me](http://www.r4i-gold.me)) (YSMenu (non il processo di scorciatoia) rende inutilizzabile la card)
- R4i3D (2012)
- R4 Infinity Dual Core
- R4 SDHC
- R4 SDHC Dual-Core ([www.r4isdhc.com](http://www.r4isdhc.com/)) (YSMenu (non il processo di scorciatoia) rende inutilizzabile la card)
{% endcapture %}

<details>
    <summary>Flashcard supportate</summary>
    <div class="details-content">
        {{ flashcards | markdownify }}
    </div>
</details>

PC:
- Un OS a 64 bit
- [Forwarder3-DS](https://www.dropbox.com/s/b9de5ii6vm3dxfn/Forwarder3DS-v2.9.6.zip?dl=0)
- Aggiornamento Java 8 251
- **Utenti Linux:** JavaFX

### Parte 1: Per Iniziare
{% capture tab-sd-card %}
1. Scarica il pacchetto [scorciatoia della scheda SD](https://www.dropbox.com/s/k5uaa4jzbtkgm0z/DS%20Game%20Forwarder%20pack%20%283DS%20SD%20Card%29.7z?dl=0)
1. Estrae il contenuto della cartella `per la scheda SD` nella directory principale della scheda SD del tuo 3DS

Dopo aver estratto il pacchetto, è possibile modificare `sd:/_nds/nds-bootstrap.ini` e modificare le impostazioni:
- `BOOST_CPU`: Se impostata a 1, viene utilizzata la velocità TWL, quindi non ci dovrebbero essere rallentamenti
- `SOUND_FREQ`: Se impostata a 1, il suono verrà riprodotto a 48khz, invece di 32khz
{% endcapture%}

{% capture tab-flashcard %}
1. Scarica uno di questi pacchetti:
   - [Original R4/M3 Simply](https://www.dropbox.com/s/juxzri7h8bttunh/DS%20Game%20Forwarder%20pack%20%28Original%20R4%2C%20M3%20Simply%29.7z?dl=0)
   - [Acekard 2(i)/M3DS Real](https://www.dropbox.com/s/5elogf885sd62hu/DS%20Game%20Forwarder%20pack%20%28M3DS%20Real%29.7z?dl=0)
   - [DSTT / R4i Gold / R4i-SDHC / R4 SDHC Upgrade / SC DSONE](https://www.dropbox.com/s/xxfmvikwmnvsu63/DS%20Game%20Forwarder%20pack%20%28DSTT%2C%20R4i%20Gold%2C%20R4i-SDHC%2C%20SC%20DSONE%29.7z?dl=0)
   - [Acekard RPG](https://drive.google.com/file/d/0B2_1xHkEp2_6OHVuZEJwU1BKbEU/view?usp=sharing)
   - [R4iDSN / R4i Gold RTS / R4i Gold 3DS Plus](https://www.dropbox.com/s/j8nquh073k9y0h7/DS%20Game%20Forwarder%20pack%20%28R4iDSN%2C%20R4i%20Gold%20RTS%29.7z?dl=0)
   - [Ace 3DS+/Gateway Blue Card/R4iLS/R4iTT](https://www.dropbox.com/s/fd7dzhn8burcq02/DS%20Game%20Forwarder%20pack%20%28Ace3DS%2C%20GW%20Blue%20Card%2C%20R4iTT%29.7z?dl=0)
   - [SC DSTWO](https://www.dropbox.com/s/pyyg0vq8b0nmhqd/DS%20Game%20Forwarder%20pack%20%28SC%20DSTWO%29.7z?dl=0)

1. Estrai il contenuto della cartella `per Slot-1 microSD` nella root della scheda microSD della tua flashcard, e (se la cartella esiste) il contenuto della cartella `per scheda SD 3DS` nella directory principale della scheda SD del tuo 3DS.

Dopo aver estratto il pacchetto per la tua Sd, puoi modificare `sd:/_nds/ntr_forwarder.ini` per modificare le impostazioni. Questo non è possibile per le flashcard Acekard RPG, R4 DS e R4i Gold RTS.
- `NTRCLOCK`: If set to `0` or <kbd class="face">A</kbd> is held, the DSi boot screen will appear instead of the normal DS splash, and TWL clock speed is used, so lags begone
- `DISABLEANIMATION`: If set to `1` or <kbd class="face">B</kbd> is held, the DS / DSi boot screen is skipped
- `HEALTHSAFETYMSG`: If set to `1`, the boot screen's health and safety message will appear on the bottom screen, otherwise the bottom screen stays white with no health and safety message
{% endcapture %}

<div class="tab-container">
    <div class="pb-3">
        <a class="tab-link btn btn-outline-secondary tab-default" href="#tab-sd-card" onclick="openTab(event, event.currentTarget)" data-tab-name="sd-card">SD Card</a>
        <a class="tab-link btn btn-outline-secondary" href="#tab-flashcard" onclick="openTab(event, event.currentTarget)" data-tab-name="flashcard">Flashcard</a>
    </div>
    <div id="tab-sd-card">
        <noscript><h4>SD Card</h4></noscript>
        {{ tab-sd-card | markdownify }}
    </div>
    <div id="tab-flashcard">
        <noscript><h4>Flashcard</h4></noscript>
        {{ tab-flashcard | markdownify }}
    </div>
</div>

### Part 2: Getting the AP fix files from TWiLight Menu++
If you already have TWiLight Menu++, skip to the next section.
1. Download the latest `TWiLightMenu-3DS.7z` from the [release page](https://github.com/DS-Homebrew/TWiLightMenu/releases)
1. In the 7z file, go to `_nds/TWiLightMenu/`
1. Copy the `apfix` folder to `sd:/_nds/ntr-forwarder/` on your 3DS's SD card

### Part 3: Forwarder3-DS
1. Open `Forwarder3DS.jar`
   - If it doesn't open, make a new text file in the same folder as Forwarder3DS.jar containing `java -jar Forwarder3DS.jar` and save it as `Forwarder3DS.bat` and run that (make sure there is no `.txt` at the end)
1. Set your card as the `Target` on the left
   - **NOTE:** If you don't see a list of cards, download [this zip](https://github.com/Olmectron/olmectron.github.io/archive/master.zip), and put the `forwarders` folder in the same folder as Forwarder3DS.jar, then rename it to `.forwarders`
1. Enable `Automatically set ROM path`
   - **Linux users:** The automatic path is incorrect since it includes the entire path (e.g. `/media/$USER/something/`), please remove that part
   - **MacOS users:** The automatic path is incorrect since it includes `/Volumes/(cardname)/` at the start, please remove that part
1. Click the folder in the top right and select the ROMs you want to make forwarders for or drag and drop them onto the window
   - **NOTE:** The ROMs must already be on your SD card when selecting them, and can't be moved without recreating the forwarders
   - **SD card users:** If your save file is in the same folder as the ROM, move it to a folder called `saves`, with the `saves` folder being in the same place as the ROMs
1. If you're playing a hack / translation of a DSi-Enhanced game that has it's banner / title edited, find the banner for the game from [here](https://www.dropbox.com/sh/igr47pr0q5bh4p5/AAA9Dy8VOGfBLUA6KdLDSDW-a?dl=0), right click on the game in Forwarder3-DS, click `Import banner`, and click on the banner to use
1. If using a homebrew ROM, click on it, then clear the `Game title` and type the game's title
1. Click the floppy disk button to generate the forwarder CIA(s)
1. Copy the CIA(s) to your 3DS's SD card, then install them using FBI
   - If using EmuNAND, install to both SysNAND and EmuNAND
