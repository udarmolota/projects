# Projects

The list of my projects that the launchers show on their **Projects** screen
(Zomdroid first). Each launcher reads `projects.json` from this repository, so a new
project or a changed link reaches every player without a launcher release.

## projects.json

```json
{
  "reddit": "https://www.reddit.com/r/UdarMolotaDev",
  "projects": [
    {
      "name": "ValDroid",
      "description": { "en": "A launcher that runs Valheim on Android.", "ru": "..." },
      "icon": "https://raw.githubusercontent.com/udarmolota/projects/main/icons/project_valdroid.png",
      "github": "udarmolota/ValDroid"
    }
  ]
}
```

- `description`: a plain string, or one per language (`en`, `ru`, `zh`, `pt`, `in`); `en` is
  the fallback.
- `icon`: an https link to a picture in `icons/` (about 192×192 PNG), or the name of a picture
  built into the launcher.
- `github`: `owner/repo`. Gives the Download button (latest release) and the version shown on the card.
- `url` (optional): the page the Page button opens; the GitHub repository by default.

The launcher keeps the last list that loaded and parsed, so a broken file never empties the
screen. Check the JSON before committing (any JSON validator).
