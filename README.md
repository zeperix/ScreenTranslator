# Screen Translator

**The project is almost abandoned. I don't have time for it and I can only fix minor issues**

## Introduction

This software allows you to translate any text on screen.
Basically it is a combination of screen capture, OCR and translation tools.
Translation is currently done via online services.

## Installation

**Windows**: download archive from [github releases](https://github.com/OneMoreGres/ScreenTranslator/releases) page, extract it and run `.exe` file.

If the app fails to start complaining about missing dlls or there are any update errors related to SSL/TLS then install or repair `vs_redist*.exe` from the release archive.

**Linux**: download `.AppImage` file from [github releases](https://github.com/OneMoreGres/ScreenTranslator/releases), make executable (`chmod +x <file>`) and run it.

**OS X**: currently not supported.

## Setup

The app doesn't have a main window.
After start it shows only the tray icon.

If the app detects invalid settings, it will show the error message via system tray.
It will also highlight the section name in red on the left panel of the settings window.
Clicking on that section name will show a more detailed error message in the right panel (also in red).

The packages downloaded from this site do not include resources, such as recognition language packs or scripts to interact with online translation services.

To download them, open the settings window and go to the `Update` section.
In the right panel, expand the `recognizers` and `translators` sections.
Select preferred items, then right click and choose `Install/Update`.
After the progress bar reaches `100%`, the resource's state will change to `Up to Date`.

You must download at least one `recognizers` resource and one `translators` resource.

After finishing downloads, go to the `Recognition` section and update the default recognition language setting (the source to be translated).
Then go to the `Translation` section, update the default translation language setting (the language to be translated into) and enable some or all translation sevices (you may also change their order by dragging).

After that all sections in the left panel should be black.
Then click `Ok` to close settings.

### Third party enhancements

**Not tested or reviewed by me**

* to translate with online AI services use scripts from [here](https://github.com/Suki8898/Translator)

* to install Hebrew translation of the app itself (thanks to [Y-PLONI](https://github.com/Y-PLONI)),
download [this](https://github.com/OneMoreGres/ScreenTranslator/releases/download/3.3.0/screentranslator_he.qm)
file and place it into the `translations` folder next to `screen-translator.exe`.

## Usage

1. Run program (note that it doesn't have main window).
2. Press capture hotkey.
3. Select region on screen. Customize it if needed.
4. Get translation of recognized text.
5. Check for updates if something is not working.

## FAQ

By default resources are downloaded to the one of the user's folders.
If `Portable` setting in `General` section is checked, then resources will be downloaded to the app's folder.

Set `QTWEBENGINE_DISABLE_SANDBOX=1` environment variable when fail to start due to crash.

Answers to some frequently asked questions can be found in issues or
[wiki](https://github.com/OneMoreGres/ScreenTranslator/wiki/FAQ)

## Limitations

* Can not capture some dynamic web-pages/full screen applications

## Dependencies

* see [Qt 5](https://qt-project.org/)
* see [Tesseract](https://github.com/tesseract-ocr/tesseract/)
* see [Leptonica](https://leptonica.com/)
* several online translation services

## Build from source

Look at the scripts (python3) in the `share/ci` folder.
Normally, you should only edit the `config.py` file

Build dependencies at first, then build the app.

## Attributions

* icons made by
[Smashicons](https://www.flaticon.com/authors/smashicons),
[Freepik](https://www.flaticon.com/authors/freepik),
from [Flaticon](https://www.flaticon.com/)
