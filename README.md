# OrisApp_changeLog

Veřejný changelog (release notes) pro [ORISapp](https://github.com/Yhdista/OrisApp) — hlavní repo je
privátní, takže appka čte `release_notes.json` odtud (`raw.githubusercontent.com` u privátních repo
bez autentizace vrací 404).

`ChangelogSyncWorker` v appce stahuje tenhle soubor jednou denně, porovná `versionCode` proti aktuální
verzi appky a nepřečtené položky promítne do "Co je nového?" v appce.

## Formát

```json
[
  {
    "version": "3.2.4",
    "versionCode": 241028,
    "date": "8. 7. 2026",
    "items": [
      { "text": "Text položky changelogu, emoji na začátku volitelné." }
    ]
  }
]
```

Nová verze appky = nová položka v poli (přidat na konec, `versionCode` musí odpovídat
`orisapp/build.gradle.kts` `versionCode` v OrisApp repu).
