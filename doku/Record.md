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
`rico:scopeAndContent` | string | Hauptinhalt und hervorzuhebender Inhalt | DE:DARIN, DE:ENTHAELT / ISAD(G): 3.3.1
`rico:type` | string | Inhaltsart (Archivalienart) | DE:ARCHIVALIENART / ISAD(G): 3.1.5, 3.3.5 (?)
`rico:conditionsOfAccess` | string | Zugangsbestimmungen | DE:ZUGANGSBESTIMMUNGEN
`rico:conditionsOfUse` | string | Benutzungsbedingungen | DE:ZUGAENGLICHKEIT_NM
`rico:isAssociatedWithDate` | URI | Entstehungszeitraum | ISAD(G): 3.1.3
`dcterms:isReferencedBy` | URL | Eintrag im öffentlichen Archivkatalog | -
`rico:history` | string | Geschichte (des Bestands, Archivs, der Provenienzstelle, etc.) | DE:ARCHIVGESCHICHTE, DE:VERWALTUNGSGESCHICHTE_BIOGRAFI / ISAD(G): 3.2.2, 3.2.3
`rico:hasOrHadMainSubject` | URI | Thematische Beziehung zu `:Place` oder `Agent` | -
`rico:resultsOrResultedFrom` | URI | Beziehung zur Ablieferung (`:Event`) | -
`rico:hasRecordSetType` | URI | Verweis auf lokal verwendete Record Set-Typen (`stabs-rst`), entspricht den Verzeichnungsstufen des Staatsarchivs | DE:STUFE / ISAD(G): 3.1.4
`rico:isOrWasIncludedIn` | URI | Verweis auf umfassenden bzw. diesen enthaltenden `:Record`, entspricht der übergeordneten Verzeichnungsstufe | DE:PARENT_ID / ISAD(G): 2.3, 3.1.4
`rico:hasProvenance` | string | Bezeichnung der Provenienzstelle | DE:AKTENBILDNER_PROVENIENZ_TEXT / ISAD(G): 3.2.1
