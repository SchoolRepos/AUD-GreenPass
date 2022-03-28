Anforderungen: 

* 4 Seiten
* Funktionsweise von unserem System (inkl. Architektur und Sequenzdiagramm)
* Umsetzungsschwierigkeiten / Schwachstellen
* Kosten und Datenschutz 

# Pflichtenheft

*Gruppe Aigner, Wimmer, Scheiböck, Mayr und Aspöck*

## Funktionsweise von unserem System

Es wird ein Token erstellt, der der GreenCheck App über die Schnittstelle von [Elga](https://secure.gesundheit.gv.at/gruenerpass/zertifikate) die Daten zur Überprüfung zur Verfügung stellt. Mit dem Token kann man dann öffentlich das Zertifikat kontrollieren (Name, Datum und Gültigkeit).

Im QR-Code ist dann nur noch der Token im [JWT-Format](https://jwt.io/) vorhanden.

Für den Check ist zwingend eine Internetverbindung notwendig.
Der Token im QR-Code und die lokalen Daten werden gecached und alle 24 Stunden neu über das Internet validiert.




## Umsetzungsschwierigkeiten / Schwachstellen

Schwachstelle könnte sein, dass die Elga-Server down gehen - zu viele Requests und Rechenzentrum nicht in Cloud.

## Kosten und Datenschutz 

Der Datenschutz ist zwar Fraglich, da jeder mit dem Token theoretisch das Zertifikat abfragen kann, jedoch ist es beim alten System auch nicht besser.
Kosten würden nur anfallen, wenn man endlich eine ordentliche Infrastruktur zur Verfügung stellen möchte.
