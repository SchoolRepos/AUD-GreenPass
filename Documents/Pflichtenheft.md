Anforderungen: 

* 4 Seiten
* Funktionsweise von unserem System (inkl. Architektur und Sequenzdiagramm)
* Umsetzungsschwierigkeiten / Schwachstellen
* Kosten und Datenschutz 

# Pflichtenheft

*Gruppe Aigner, Wimmer, Scheiböck, Mayr und Aspöck*

## Funktionsweise von unserem System

Unser System basiert darauf, dass im QR-Code selbst keine Daten vorhanden sind, sondern nur ein Token im [JWT-Format](https://jwt.io/). Beim Scannen durch z.B. Security-Personal wird eine Validierungs-Anfrage an eine [Elga](https://secure.gesundheit.gv.at/gruenerpass/zertifikate)-Schnittstelle geschickt, die dann das Zertifikat zurücksendet. Hierdurch wird gewährleistet, dass das Zertifikat sehr schwer zu fälschen ist. 
Außer dieser Änderung des Inhalts des QR-Codes bleibt die momentane Architektur zum Großteil erhalten.

![AddCertificate](https://user-images.githubusercontent.com/71697714/161512649-542894a0-d803-4cb8-a8b2-48a6474c87d9.png)

## Umsetzungsschwierigkeiten / Schwachstellen

Grundsätzlich gibt es rein Programmiertechnisch nicht viele Hürden, besonders da die Architektur nicht zu sehr verändert wird. Für den Check ist jedoch zwingend eine Internetverbindung notwendig, was in ländlichen Gebieten schwer sein könnte - eine Alternative könnte sein, dass die Validierung ab Abruf 24 Stunden auch offline gültig ist, was aber wieder Sicherheitsrisiken mit sich birgt.

Weiters wäre es problematisch, wenn die Elga-Server ein Problem mit den vielen Requests bekommen würden - besonders, da das Rechenzentrum nicht in der Cloud ist, und daher nicht schnell skalieren kann. Hierbei sollten mehrere Schnittstellen, sowie eine Cloud-basierte Architektur erdacht werden.
Auch muss auf Privatsphäre geachtet werden - obwohl nur ein Token übertragen wird sollte zur Sicherheit die Verbindung trotzdem gut verschlüsselt sein.

## Kosten und Datenschutz 

Der Datenschutz ist zwar fraglich, da jeder mit dem Token theoretisch das Zertifikat abfragen kann, jedoch ist es beim alten System auch nicht wirklich besser - und unserere Version ist fälschungsresistänter. 
Kosten würden nur für evtl. Infrastrukturänderungen anfallen, da z.B. die UI weiterverwendet werden kann.
