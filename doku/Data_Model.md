# Datenmodell für <ld.staatsarchiv.bs.ch>

Frei verfügbare Inhalte des Archivsystems scopeArchiv des Staatsarchivs Basel-Stadt werden in ein RDF-basiertes Datenmodell konvertiert. Das Datenmodell basiert auf der archivspezifischen Ontologie [Records in Context](https://www.ica.org/standards/RiC/ontology) des International Council on Archives. Hier werden dokumentiert:
* Die wichtigsten Klassen
* Die jeweiligen Eigenschaften (properties)
* Die Datenelemente des Quellsystems scopeArchiv
* Wo möglich, einen Verweis auf die Herkunft im Standard ISAD(G)

## Verwendete Vokabulare

Präfix | Namespace IRI | Definition
--- | --- | ---
\- | <https://ld.staatsarchiv.bs.ch/> | Namensraum für referenzierte Entitäten des Staatsarchivs (Data URI)
`admin` | <http://schema.ld.admin.ch/> | Namensraum des Swiss Confederation Linked Data Schema
`dcterms` | <http://purl.org/dc/terms/> | Namensraum für Dublin Core Terms
`owl` | <http://www.w3.org/2002/07/owl#> | Namensraum für OWL
`rico` | <https://www.ica.org/standards/RiC/ontology#> | Namensraum der Records in Context-Ontologie
`ric-dft`	| <https://www.ica.org/standards/RiC/vocabularies/documentaryFormTypes#> |	ICA RiC Documentary Form Types vocabulary namespace
`ric-rst` | <https://www.ica.org/standards/RiC/vocabularies/recordSetTypes#> | ICA Record Set Types vocabulary namespace
`schema` | <http://schema.org/> | Namensraum für schema.org
`skos` | <http://www.w3.org/2004/02/skos/core#> | Namensraum für SKOS
`stabs-idt` | https://ld.staatsarchiv.bs.ch/vocabularies/IdentifierTypes# | Namensraum für lokal verwendete Typen von Identifikatoren (v.a. Signaturtypen)
`stabs-ext` | <https://ld.staatsarchiv.bs.ch/vocabularies/ExtentTypes#> | Namensraum für lokal verwendete Umfangsangaben
`stabs-rst` | <https://ld.staatsarchiv.bs.ch/vocabularies/recordSetTypes#> | Namensraum für lokal verwendete Record Set Types
`stabs-tht` | <https://ld.staatsarchiv.bs.ch/vocabularies/thesaurusTypes#> | Namensraum für lokal verwendete Thesauri-Typen
`xsd` | <http://www.w3.org/2001/XMLSchema#> | XML Schema namespace

## Verwendete Konzepte

* [:Record](Record.md): Klasse `rico:RecordResource` mit den Subklassen `rico:RecordSet` und `rico:Record`
* [:Agent](Agent.md): Klassen `rico:Agent` und `skos:Concept`
* [:Place](Place.md): Klassen `rico:Place` und `skos:Concept`
* [:Event](Event.md): Klasse `rico:Activity`
* [:Rule](Rule.md): Klasse `rico:Rule`
* [:Instantiation](Instantiation.md): Klasse `rico:Instantiation`