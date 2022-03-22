# Vibrant Venture Localization
This is a public repository for localization of Semag Games' video game [Vibrant Venture](https://store.steampowered.com/app/1264520/Vibrant_Venture/).

[Join our Discord server](https://discord.gg/semag-games) to be a part of the community!

## Dialogue
The `dialogue` directory contains all the files for the in-game dialogue and responses. Dialogue is stored in the `.json` format.
Forced line-breaks are included in some dialogue for comedic effect or to convey a specific tone. These are denoted using the special character `\n`.
Dialogue also includes special tags with a syntax similar to common markup languages:
- `<c>` for colored text.
  - Color tags have a number of presets - for example, to color the text `Hello!` with Violastro's color, you would write `<c=violastro>Hello!</c>`.
  - Color tags also allow RGB codes - for example, to color the text `Hello!` with in yellow, you would write `<c=255,255,0>Hello!</c>`.
- `<s>` for shaking text.
- `<w>` for wavy text.

When working with dialogue, please **make sure to also include these tags in the localized dialogue whenever they are used.**
In addition, **make sure to use the correct locale code (`en` for English, for example) and ensure that locales are listed alphabetically**.

## XLIFF
The `xliff` directory contains all the files for the in-game menus, HUDs, etc. - essentially, everything besides the dialogue. 
Some of these files use special tags for in-game formatting - **please ensure that these are also included in translated text, and that the names of variables remain the same.**
For example, in `Tutorials_da.xlf`, one of the English entries include a tag for coloring the Double Jump tutorial text: 

`Press {0} while airborne to <color={characterColor}>Double Jump</color>`

**Do not translate variables like `characterColor`.**

Do not translate `Steam Workshop` - Valve themselves do not translate the name of the Steam Workshop so we don't either.

Make sure that the double quotation mark comma separation style is followed when making changes. 
I recommend using the free and open source editor Poedit for working with the XLIFF files.
[You can find it here](https://poedit.net/).
