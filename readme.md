# StABS-scope2RDF
Dieses Repository enthält die Transformation der öffentlichen Daten aus dem Archivsystem scopeArchiv des [Staatsarchivs Basel-Stadt (StABS)](https://www.staatsarchiv.bs.ch/) in ein RDF-Modell in der Ontologie [Records in Context Ontology v.02 (RiC-O)](https://github.com/ICA-EGAD/RiC-O/) des [International Council on Archives (ICA)](https://www.ica.org).

* Ein erstes Mapping von Materialised Views der Oracle-Datenbank von scopeArchiv erfolgt mittels [R2RML](https://www.w3.org/TR/r2rml). Dieses R2RML-Mapping wird mit [Zazukos](https://zazuko.com/) ["Expressive RDF Mapper (XRM)"](https://github.com/zazuko/expressive-rdf-mapper) erstellt. XRM-Dateien befinden sich im Ordner [/src](/src/), die R2RML-Datei ist [/src-gen/mapping-stabs.r2rml.ttl](/src-gen/mapping-stabs.r2rml.ttl).
* In einem zweiten Schritt wird in einem internen Triple-Store ([stardog free](https://www.stardog.com)) eine Serie von SPARQL-Updates (insert, delete) durchgeführt. Diese befinden sich im Ordner [/sparql](/sparql/).
* Für die Publikation im öffentlichen Triplestore ([ld.staatsarchiv.bs.ch](https://ld.staatsarchiv.bs.ch)) werden Metadaten und Vokabulare ergänzt. Diese befinden sich im Ordner [/metadata](/metadata/).
* Das Repository enthält ebenfalls eine Dokumentation des Datenmodells im [Wiki](https://github.com/Staatsarchiv-Basel-Stadt/StABS-scope2RDF/wiki).

# Pipeline

* Die Transformationen werden in einer [ETL-Pipeline](https://de.wikipedia.org/wiki/ETL-Prozess) verwendet. Der Code befindet sich im Repository [RDF-Pipeline](https://github.com/Staatsarchiv-Basel-Stadt/RDF-Pipeline), die Pipeline basiert auf Zazukos [barnard59-toolkit](https://github.com/zazuko/barnard59).
* Der interne Triplestore mit einer Verbindung zur Oracle-Datenbank erfolgt mit stardog. Der Code für diese Dienste befindet sich im Repository [stardog-docker](https://github.com/Staatsarchiv-Basel-Stadt/stardog-docker).

# Branches

* Der Branch [main](https://github.com/Staatsarchiv-Basel-Stadt/StABS-scope2RDF/tree/main) ist die produktive Transformation. Sie wird täglich für die Publikation angewendet.
* Der Branch [development](https://github.com/Staatsarchiv-Basel-Stadt/StABS-scope2RDF/tree/development) wird für die interne Entwicklung genutzt.
* Ein alter Branch [xisadgr-archive](https://github.com/Staatsarchiv-Basel-Stadt/StABS-scope2RDF/tree/xisadgr-archive) enthält ein nicht weitergeführtes Mapping in die [xIsadgR ontology](https://github.com/KOST-CECO/ontologies) der [KOST](https://kost-ceco.ch). 

