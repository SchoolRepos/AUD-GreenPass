Anforderungen: 

* 4 Seiten
* Funktionsweise von unserem System (inkl. Architektur und Sequenzdiagramm)
* Umsetzungsschwierigkeiten / Schwachstellen
* Kosten und Datenschutz 

# Pflichtenheft

*Gruppe Aigner, Wimmer, Scheiböck, Mayr und Aspöck*

## Funktionsweise von unserem System

Es wird ein Token erstellt, der der GreenCheck App über die Schnittstelle von [Elga](https://secure.gesundheit.gv.at/gruenerpass/zertifikate) die Daten zur Überprüfung zur Verfügung stellt. Mit dem Token kann man dann öffentlich das Zertifikat kontrollieren (Name, Datum und Gültigkeit). Hierdurch wird gewährleistet, dass das Zertifikat sehr schwer zu fälschen ist. Außer dieser Änderung des Inhalts des QR-Codes bleibt die momentane Architektur zum Großteil erhalten. 

Im QR-Code ist dann nur noch der Token im [JWT-Format](https://jwt.io/) vorhanden. 

Für den Check ist zwingend eine Internetverbindung notwendig. Der Token im QR-Code und die lokalen Daten werden gecached und alle 72 Stunden läuft das Zertifikat ab - dann muss das Zertifikat neu über das Internet validiert werden. Sollte binnen 72 Stunden keine Internetverbindung bestehen wird das Zertifikat als abgelaufen angezeigt.

Außer dieser Änderung des Inhalts des QR-Codes bleibt die momentane Architektur zum Großteil erhalten.

![AddCertificate](https://user-images.githubusercontent.com/71697714/161512649-542894a0-d803-4cb8-a8b2-48a6474c87d9.png)

## Umsetzungsschwierigkeiten / Schwachstellen

Grundsätzlich gibt es rein Programmiertechnisch nicht viele Hürden, besonders da die Architektur nicht zu sehr verändert wird. Für den Check ist jedoch zwingend eine Internetverbindung notwendig, was in ländlichen Gebieten schwer sein könnte - eine Alternative könnte sein, dass die Validierung ab Abruf 72 Stunden auch offline gültig ist, was aber wieder Sicherheitsrisiken mit sich birgt. Ohne Internetverbindung wird das beständige Problem der Validierung nicht lösbar sein.

Weiters wäre es problematisch, wenn die Elga-Server ein Problem mit den vielen Requests bekommen würden - besonders, da das Rechenzentrum nicht in der Cloud ist, und daher nicht schnell skalieren kann. Hierbei sollten mehrere Schnittstellen, sowie eine Cloud-basierte Architektur erdacht werden.
Auch muss auf Privatsphäre geachtet werden - obwohl nur ein Token übertragen wird sollte zur Sicherheit die Verbindung trotzdem gut verschlüsselt sein.

## Kosten und Datenschutz 

Der Datenschutz ist zwar fraglich, da jeder mit dem Token theoretisch das Zertifikat abfragen kann, jedoch ist es beim alten System auch nicht wirklich besser - und unserere Version ist fälschungsresistänter. 
Kosten würden nur für evtl. Infrastrukturänderungen anfallen, da z.B. die UI weiterverwendet werden kann.
