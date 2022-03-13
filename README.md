# Vibrant Venture Localization
This is a public repository for localization of Semag Games' video game [Vibrant Venture](https://store.steampowered.com/app/1264520/Vibrant_Venture/).

[Join our Discord server](https://discord.gg/semag-games) to be a part of the community!

## Dialogue
The `dialogue` directory contains all the files for the in-game dialogue and responses. Dialogue is stored in the `.json` format.
Forced line-breaks are included in some dialogue for comedic effect or to convey a specific tone. These are denoted using the special character `\n`.
Dialogue also includes special tags with a syntax similar to common markup languages:
- `<c>` for colored text
  - Color tags have a number of presets - for example, to color the text `Hello!` with Violastro's color, you would write `<c=violastro>Hello!</c>`.
  - Color tags also allow RGB codes - for example, to color the text `Hello!` with in yellow, you would write `<c=255,255,0>Hello!</c>`.
- `<s>` for shakey text
- `<w>` for wavey text

When working with dialogue, please **make sure to also include these tags in the localized dialogue whenever they are used.**
In addition, **make sure to use the correct locale code (`en` for English, for example) and ensure that locales are listed alphabetically**.

## CSV
The `csv` directory contains all the files for the in-game menus, HUDs, etc. - essentially, everything besides the dialogue. 
Some of these files use special tags for in-game formatting - **please ensure that these are also included in translated text, and that the names of variables remain the same.**
For example, in `Tutorials.csv`, one of the English columns include a tag for coloring the Double Jump tutorial text: 

`Press {0} while airborne to <color={characterColor}>Double Jump</color>`

**Do not translate variables like `characterColor`.**
Make sure that the double quotation mark comma separation style is followed when making changes. 

I recommend using Visual Studio Code with the "Edit csv" extension [which can be found here](https://marketplace.visualstudio.com/items?itemName=janisdd.vscode-edit-csv).

If you decide to use VSCode with this extension for editing, make sure to enable the "Quote all fields" setting: 
![image](https://user-images.githubusercontent.com/57709490/158064363-2a040cce-c538-4e46-b61e-056da04d7991.png)
