---
lang: en-US
layout: wiki
section: twilightmenu
category: updating
title: Updating (3DS)
description: How to update TWiLight Menu++ on the Nintendo 3DS
---

If updating from a version older than v16.4.0, please move your `.sav` files for DS games to a new folder called `saves`, with the `saves` folder being in the same place as the DS roms.
{:.alert .alert-info}

{% capture tab-universal-updater %}
1. Open Universal-Updater
   - If you don't have it, follow the [installing](installing-3ds) instructions
1. Find TWiLight Menu++ in the app grid, you can search with the 3rd tab on the sidebar if you have trouble finding it
1. Press <kbd class="face">A</kbd> or tap the download icon in the sidebar and select `TWiLight Menu++` to install it
   - This will take a while
{% endcapture %}

{% capture tab-manual %}
1. Download the latest version of `TWiLightMenu-3DS.7z` from [the releases page](https://github.com/DS-Homebrew/TWiLightMenu/releases)
1. Extract `TWiLightMenu-3DS.7z`
1. Copy the `_nds` folder to your SD card root
1. Copy the `BOOT.NDS` file to your SD card root
1. Copy the two `.cia` files to your SD card root
1. On your 3DS, install the two CIAs with FBI
{% endcapture %}

### Updating
<div class="tab-container">
   <div class="pb-3">
      <a class="tab-link btn btn-outline-secondary tab-default" href="#tab-universal-updater" onclick="openTab(event, event.currentTarget)" data-tab-name="universal-updater">Universal-Updater</a>
      <a class="tab-link btn btn-outline-secondary" href="#tab-manual" onclick="openTab(event, event.currentTarget)" data-tab-name="manual">Manual</a>
   </div>
   <div id="tab-universal-updater">
      <noscript><h4>Universal-Updater</h4></noscript>
      {{ tab-universal-updater | markdownify }}
   </div>
   <div id="tab-manual">
      <noscript><h4>Manual</h4></noscript>
      {{ tab-manual | markdownify }}
   </div>
</div>

### More steps for the flashcard side

If you can switch between the SD and flashcard contents in TWLMenu++, and if the flashcard TWLMenu++ is on v16.3.0 or later, please follow these steps.

1. Go into TWLMenu++ Settings
1. Select `Update TWiLight Menu++`
1. Select `Console (micro)SD > Slot-1 microSD`
