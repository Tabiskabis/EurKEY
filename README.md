# EurKEY

Ports and variants for Mac and Windows, based on [EurKEY keyboard layout by Steffen Brüntjen](http://eurkey.steffen.bruentjen.eu/) - The Keyboard Layout for Europeans, Coders and Translators


## Mac variants

### `EurKEY.keylayout`

Fork of [Leonardo Brondani Schenkel's](https://github.com/lbschenkel/EurKEY-Mac) EurKEY, updated to v1.3 as designed by Steffen Brüntjen.  
This version appears to be optimised for physical ANSI style keyboards.

### `EurKEY-iso.keylayout`

For usage with ISO style physical keyboards. Swapped the `§` and `Gravis` keys (leftmost of number row and bottom row, key not available on ANSI keyboards).

### `EurKEY-iso-qwertz.keylayout`

Swapped the `Z` and `Y` keys. For use in QWERTZ dominated places.


## Windows variants

Windows seems to be less picky about the physical keyboard style, so there is no ISO variant.  
It has a bunch of other oddities, though. One being that keyboard layouts are associated with a locale (=language).

### `EurKEY.klc`

DLL name: `eurkey`  
Updated to version v1.3 as designed by Steffen Brüntjen, yet **bugged**: The dead key state `shift + altGr + m` does not work.

### `EurKEY-iso.klc`

DLL name: `eurkeyi`  
Like the Mac -iso version, this one is optimised for ISO style physical keyboards, i.e. the additional bottom left key produces `§`/`±`. This closer reflects the original US layout than the US-International.

### `EurKEY-iso-qwertz.klc`

DLL name: `eurkezi`  
Swapped the `Z` and `Y` keys. For use in QWERTZ dominated places.  
Undo and redo ***feel*** *buggy*. The en-US locale apparently determines the undo and redo shortcuts in Windows. That makes ctrl-y undo and ctrl-z redo. So undo/redo are physically located where it's expected on QWERTY keyboards.

### `EurKEY-iso-qwertz-sg.klc`

DLL name: `eurkezsg`  
Based on the de-CH locale (why yes, I'm swiss), this variant counters the awkward undo/redo situation mentioned above.  
Additionally, `altGr + §` produces `\` as on the `Swiss (German)` Layout.  
As a side effect, installing this variant adds the language `German (Switzerland)` to the system. It can be removed and the layout added to whatever other language, but that must be done manually in Windows' Settings app.


## Installation

### macOS

Copy the two files `EurKEY.keylayout` and `EurKEY.icns` to your library, either system-wide (`/Library/Keyboard Layouts`) or for your local user (`~/Library/Keyboard Layouts`). A system-wide installation is preferred though to ensure the layout is available to all applications. (See also [this Superuser answer](https://superuser.com/a/561613/263461).)

### Windows

Use [Microsoft Keyboard Layout Creator](https://www.microsoft.com/en-us/download/details.aspx?id=102134) to build an installer from a .klc file.  
I will not publish binary files.


## License

The Layout itself is licensed under [GPLv3](http://www.gnu.org/licenses/gpl-3.0.html).  
The EU flag icon is taken from [Iconspedia](http://www.iconspedia.com/pack/european-flags-1631/),
created by [Alpak](http://alpak.deviantart.com/) and
licensed under [CC](http://creativecommons.org/licenses/by-nc-nd/3.0)
