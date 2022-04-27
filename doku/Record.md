# Entität *Record*
## Schema der URI

```
https://ld.staatsarchiv.bs.ch/Record/[id]
```

## Klassen

Klasse | Verwendung | Quelle
--- | --- | ---
`rico:RecordResource` | als Superklasse für alle "Record-Ressourcen" verwendet | Sämtliche Verzeichnungseinheiten aus scopeArchiv
`rico:RecordSet` | als spezifische Klasse für alle "Record-Ressourcen", die ein Set beschreiben | Verzeichnungseinheiten der Verzeichnungsstufen "Archiv", "Abteilung", "Fonds", "Bestand", "Serie" und "Dossier"
`rico:Record` | als spezifische Klasse für alle "Record-Ressourcen", die ein Dokument beschreiben | Verzeichnungseinheiten der Verzeichnungsstufe "Dokument"

## Eigenschaften

property | Datentyp | Inhalt | Quelle 
--- | --- | --- | --- 
`rico:title` | string | Titel | DE:TITEL / ISAD(G): 3.1.2
`rico:identifier` | string | Signatur | DE:SIGNATUR / ISAD(G): 3.1.1