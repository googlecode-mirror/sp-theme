# Introduction #

_The following borrows heavily under the terms of the GPL v2 license from both [the process and the text created by Scott Wallick for the Sandbox theme](http://code.google.com/p/sandbox-theme/wiki/SandboxInYourLanguage)._

This document explains how to use, and how to create and edit, translations of the theme. Check with [the tip of the code repository](http://code.google.com/p/sp-theme/source/browse/) before you begin, to make sure that a translation for the same language/geography pair is not in progress, and to ensure you're translating the most current theme text.

To add or improve a translation, check the [Issues tab](http://code.google.com/p/sp-theme/issues/list), then create a new Issue, attaching either your new `.po` and `.mo` files, or a _patch_(1) that adds or changes the appropriate files and directories.

# Details #

## Using a provided translation ##

Existing localizations ship with stable releases of the Sp theme. To use a provided translation, set your desired language in the Habari admin panel's **Options** section.

## Creating a new translation ##

  1. The file you want to translate is `sp/locale/sp.pot`. It is included in the Sp distribution, but you should use the latest version at http://code.google.com/p/sp-theme/source/browse/locale/sp.pot to ensure currency.
  1. Use the `sp.pot` template to create your own plain-text localization file (`*.po`) and its binary form (`*.mo`). _Poedit_ is a tool for this translation process; see http://www.poedit.net. Habari convention is to sort localizations into directories named with the lower-case form of their country/geo pair, each containing a directory `LC_MESSAGES`, which in turn contains the language files. For example, `sp/locale/fr-fr/LC_MESSAGES/sp.mo` is the binary gettext localization for the "French, France" language.

Once you have finalized your translation, [create a new Issue](http://code.google.com/p/sp-theme/issues/entry) (on the Issues tab) and attach your `.po` and `.mo` files. The Issue should describe precisely the _language, geography_ pair for which you have translated. (NB: `.mo` files are easily generated & this part of the process should probably change to only request the text `.po`.)

State the release version or _hg_ revision of Sp on which you based your localization.

## Improving an existing translation ##

To improve, correct, update, or create a country/region variant of an existing localization, download the nearest-match `.po` file from the `sp/languages/` directory, if any, and edit as described above, attaching the resulting sp.po file to a new Issue to let the project know about it.

## Synchronizing a translation with the latest version of Sp ##

Translations can be mechanically updated with the latest Sp strings template. To do so, obtain the translation you want to update, along with the `sp.pot` file from the tip of the source repository.
  1. Open the old `.po` file in Poedit (eg. `locale/fr-fr/LC_MESSAGES/sp.po`).
  1. Select _Catalog_ > _Update from POT file ..._
  1. Select the `locale/sp.pot` file in the resulting dialog.
  1. Poedit adds new items to translate, and pares those strings no longer in use.
  1. Translate any new or significantly modified strings as for a new translation.
  1. Attach the resulting `.po` file to an issue as for a new translation, above.

## See also ##
  * http://wiki.habariproject.org/en/Translation