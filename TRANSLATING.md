# Translating The Good Gear

Thank you for helping! Here is everything you need to know. It takes five minutes.

## The files

One file per language: `translations/<CODE>/IG_UI.json`, the codes being the game's own (`EN`, `FR`, `DE`, `PTBR`, `CN`, `CH`, `JP`…). Each line is a key and its text:

```json
"IGUI_AVC_Src_wet": "Wet",
```

**Only translate the text on the right.** Never change the key on the left (`IGUI_AVC_…`).

The reference is [`translations/EN/IG_UI.json`](translations/EN/IG_UI.json). `FR` is the other checked language, if you read French.

## The rules that matter

1. **Keep the placeholders.** `%1` and `%2` are replaced by numbers in the game: `"Your discomfort is currently %1."` shows *Your discomfort is currently 32/100.* You can move them in the sentence, but keep them all.
2. **Never write a lone `%`.** The game reads `%` as the start of a placeholder: a `%` not followed by a digit can crash the options menu. Write *percent* in words, or leave it out (the game adds the sign itself where needed).
3. **Keep it short.** The window is small. Labels (column headers, section titles, option names) should be about as long as the English ones. Sentences can wrap, but shorter is better.
4. **Use the game's words.** If your language's version of Project Zomboid already has a term (*Discomfort*, *Bite*, *Scratch*, *Desensitized*, *Heavy Load*…), use it: players will recognize it. You find them in the game folder, `media/lua/shared/Translate/<CODE>/`.
5. **Plain, friendly tone.** Speak to the player directly (*your discomfort*), as the game does.

## What each group of keys is

| Keys | Where they appear |
|---|---|
| `Title`, `Open`, `Tagline` | window title, right-click menu entry, the motto under the title |
| `Discomfort`, `Protection`, `GearLine`, `EnvLine`, `NowCurrent`, `NowRise`, `NowDrop`, `NowStay` | the two bars and the sentences around them |
| `LegendGear`, `LegendEnv` | the legend of the yellow and red markers |
| `GroupGear`, `GroupEnv`, `Rubs`, `Free`, `Region_*` | section and sub-section titles of the list |
| `Src_*` | causes of environmental discomfort (one per line, starting with a capital letter) |
| `ColDiscomfort`, `ColBite`, `ColScratch` | column headers (very short!) |
| `Holes*` | tooltip of the danger icon on damaged items |
| `Help1` to `Help5`, `HelpTitle` | tooltip of the **?** |
| `Opt*` | Options › Mods |
| `Speed`, `SpeedNone`, `ProtShort`, `MiniGear`, `EnvShort` | speed line, discreet panel |

## How to send your work

- **A few fixes**: [open a "Translation fix" issue](../../issues/new?template=translation-fix.md): the language, the key, the current text, your text.
- **A whole file, or a new language**: a pull request on `translations/<CODE>/IG_UI.json`, or attach the file to a ["New language" issue](../../issues/new?template=new-language.md).

Your translation ships with the next update of the mod, and you are credited in the changelog (tell us the name you want).
