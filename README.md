# Updates 07.04.2025:
## ImageProblem
Try to repair Problem with Images https://github.com/fastxl2024/mass-search-card/issues/1
Changed hacs-json
New Folder


## extended Translation:

            de: {
                album_label: 'Album',
                artist_label: 'Künstler',
                close_button: 'Schließen',
                dropdown_label_media_player: 'Wählen Sie einen Media Player',
                error_fetching: 'Beim Abrufen der Ergebnisse ist ein Fehler aufgetreten.',
                library_only_label: 'Lokale Bibliothek',
                media_type: 'Medientyp',
                no_results: 'Keine Ergebnisse gefunden.',
                playing_media: 'Abgespielte Medien:',
                playlist_label: 'Wiedergabeliste',
                popup_title: 'Suchergebnisse für:',
                radio_label: 'Radio',
                results_label: 'Anzahl der Ergebnisse',
                search_button: 'Suche',
                search_placeholder: 'Geben Sie hier Ihren Suchbegriff ein...',
                select_media_type: 'Medientyp auswählen',
                title_text: 'in Music Assistant suchen',
                track_label: 'Titel',
                unknown_artist: 'Unbekannter Künstler',
                unknown_duration: 'Unbekannte Dauer',
            },
## missing Translations:

        titleText.textContent = t.title_text;

line: 747
            noResults.textContent = 'No results found.';
            noResults.textContent = t.no_results;

line: 753
        closeButton.textContent = 'Close';
        closeButton.textContent = t.close_button;

line: 834
            noOption.textContent = 'Geen mediaplayers beschikbaar';
            noOption.textContent = t.error_media_player;

##New Translation needed:
suggestion
error_media_player: 'Keine Media Player verfügbar',


# Mass Search Card

The **Mass Search Card** is an advanced search card for Home Assistant, designed to simplify interaction with Music Assistant. This card allows you to effortlessly search for artists, tracks, albums, playlists, and radio stations and play them on your selected media players.
Click on the magnifying glass in the input bar to search for your item, after you select a media_player en media type.

## Features

- Supports searching for artists, tracks, albums, playlists, and radio stations.
- Dynamic dropdown selection for media players and media types.
- Popup display for search results with detailed information.
- Multi-language support (English, Dutch, Czech and Swedish).
- Easy integration with Music Assistant.

## Screenshots

<div style="display: flex; align-items: flex-start; gap: 20px;"> <img src="https://github.com/user-attachments/assets/25025169-a99e-4536-b930-e7b71fbe40a9" alt="Search Panel" width="50%"> <img src="https://github.com/user-attachments/assets/ce10cadf-bada-444a-87ea-a9d05f0a41db" alt="Search Results" width="50%"> </div>

## Installation

### HACS (Home Assistant Community Store)
1. Ensure HACS is installed in your Home Assistant setup.
2. Add this repository via HACS:
   - Go to **HACS > Integrations** and click on **+**.
   - Add the GitHub URL of this repository. (https://github.com/fastxl2024/mass-search-card.git)
3. Search for `Mass Search Card` and install the card.
4. Add the following line to your `Lovelace` resources:
   ```yaml
   resources:
     - url: /hacsfiles/mass-search-card/mass-search-card.js
       type: module

# Manual Installation
1. Download the mass-search-card.js file from this repository.
2. Place the file in the /www folder of your Home Assistant configuration.
3. Add the following line to your Lovelace resources:
   ```yaml
   resources:
     - url: /local/mass-search-card.js
       type: module

# Usage and configuration
   ````yaml
      type: custom:mass-search-card
      language: en
   ````
   **Optional Configuration:**
   ````yaml
      language: Set the language of the card. Supported languages: cz, en, nl, sv.
      Default: en
   ````

**Feel free to add some languages!**

**Known bugs:** 
- scaling of card
- no "icon" when item is in library
