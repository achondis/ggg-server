# Ressourcenpaket

| Datei | Inhalt | SHA-1 |
|---|---|---|
| `resourcepack-v2.zip` (**aktuell**) | BetterModel (Flugmounts, Dungeon-Bosse) + MMOMagic (Zauberstäbe, Schmuck, Roben, Rucksäcke) | `04443e4211e6fccdd92230f24f3e7037f82fb9ff` |
| `resourcepack.zip` (v1, alt) | nur BetterModel | `a1dad68652d6893c699f466943a3064b27debeec` |

Eintrag in `server.properties`:

```
resource-pack=https://raw.githubusercontent.com/achondis/ggg-server/resourcepack/resourcepack-v2.zip
resource-pack-sha1=04443e4211e6fccdd92230f24f3e7037f82fb9ff
require-resource-pack=true
```

## Aufbau
- `assets/bettermodel/` – von BetterModel erzeugt (`plugins/BetterModel/build.zip` auf dem Server)
- `assets/mmomagic/` – aus `plugins/MMOMagic/MMOMagic-Ressourcenpaket.zip`
- `pack.mcmeta` von BetterModel (Format 46–97)

Bei jeder Änderung (neue BetterModel-Modelle, neue MMOMagic-Texturen) beide Teile neu zusammenführen,
als neue Datei mit höherer Nummer ablegen (`resourcepack-v3.zip` …) und Link + SHA-1 in
`server.properties` anpassen. Eine neue Datei statt Überschreiben verhindert, dass GitHub für ein paar
Minuten noch die alte Version ausliefert.
