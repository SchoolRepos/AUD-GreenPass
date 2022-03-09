Anforderungen: 

* 4 Seiten
* Funktionsweise des aktuellen Systems (inkl. Architektur und Sequenzdiagramm)
* QR-Code (Inhatl, Generierung und Verifizierung)
* Schwachstellen (digital/analog)

# Analysedokument 

*Gruppe Aigner, Wimmer, Scheiböck, Mayr und Aspöck*

## Funktionsweise des aktuellen Systems

![image](https://user-images.githubusercontent.com/44428493/154077280-325734ce-d0c9-4433-8123-3ad4eedf71cd.png)

Der Grüne Pass ist ein Überbegriff für den Nachweis einer Corona-Impfung, einer durchgemachten Infektion mit Corona, oder eines negativen Testergebnisses. Die einheitliche Lösung in allen EU-Mitgliedstaaten bilden die EU Digital COVID Certificates, welche in Österreich als Testzertifikat, Genesungszertifikat und Impfzertifikat umgesetzt wurden. 
Jedes dieser Zertifikate ist mit einem EU-konformen QR-Code versehen. Dieser bildet die Grundlage für die Überprüfung durch die jeweils befugte Stelle. Die Zertifikate können einfach auf elektronischen Geräten (z.B. Smartphones) gespeichert werden. Um die Zertifikate digital abrufen zu können, ist eine Handysignatur oder Bürgerkarte notwendig, welche daher zeitgerecht beantragt werden sollten. Die Zertifikate können einerseits digital und andererseits analog (ausgedruckt) vorgezeigt werden.
Der Grüne Pass besteht einerseits aus den bereits bestehenden Nachweisen und andererseits aus drei EU-konformen Zertifikaten, die eine einfache Überprüfung einer erhaltenen Corona-Schutzimpfung (Impfzertifikat), einer durchgemachten Infektion mit SARS-CoV-2 (Genesungszertifikat) oder eines negativen Testergebnisses (Testzertifikat) ermöglichen. Die drei Zertifikate können einzeln und unabhängig voneinander abgerufen und verwendet werden.

Die Daten, die für die Erstellung der oben genannten Zertifikate notwendig sind, werden als „minimal Dataset“ bezeichnet. Neben einem EU-konformen QR-Code sind im Testzertifikat folgende Daten enthalten:

#### Inhalt Testzertifikat
- Nachname(n) und Vorname(n) der getesteten Person,
- Geburtsdatum der getesteten Person,
- Zielkrankheit oder -erreger, auf die oder den die Person getestet wurde, ausschließlich lautend auf „COVID-19“,
- Art des Tests,
- Bezeichnung des Tests,
- Bezeichnung des Herstellers des Tests,
- Datum und Uhrzeit der Probenahme,
- Testergebnis (nachgewiesen/nicht nachgewiesen)*,
- Bezeichnung des Testzentrums oder der testenden Einrichtung,
- Bezeichnung des Staates, in dem der Test durchgeführt wurde,
- Bezeichnung des Ausstellers des Testzertifikats,
- eindeutige Kennung des Testzertifikats.

#### Inhalt Genesungszertifikat
- Nachname(n) und Vorname(n) der getesteten Person,
- Geburtsdatum der getesteten Person,
- Krankheit oder Erreger, von der oder dem die Person genesen ist, ausschließlich lautend auf „COVID-19“,
- Datum des ersten positiven molekularbiologischen Testergebnisses,
- Bezeichnung des Staates, in dem der Test durchgeführt wurde,
- Bezeichnung des Ausstellers des Genesungszertifikats,
- Gültigkeitsbeginn des Genesungszertifikats,
- Gültigkeitsende des Genesungszertifikats,
- eindeutige Kennung des Genesungszertifikats.

#### Inhalt Impfzertifikat
- Nachname(n) und Vorname(n) der geimpften Person in dieser Reihenfolge,
- Geburtsdatum der geimpften Person,
- Krankheit oder Erreger, gegen die oder den die Person geimpft ist, ausschließlich lautend auf „COVID-19“,
- Impfstoff/Prophylaxe,
- Impfarzneimittel (Bezeichnung des Impfstoffs gemäß Zulassung),
- Zulassungsinhaber oder Hersteller des Impfstoffs,
-  Nummer der Impfdosis und die Gesamtanzahl der Impfdosen einer Impfserie,
   −          Das Impfzertifikat einer ersten Dosis mit einem COVID-19 Impfstoff, bei dem zwei Dosen vorgesehen sind (BioNTech/Pfizer, AstraZeneca, Moderna), enthält die Information „1 von 2“
   −          Das Impfzertifikat einer zweiten Dosis mit einem COVID-19 Impfstoff, bei dem zwei Dosen vorgesehen sind (auch bei mehrmaligen Impfstichen im Falle von „non respondern“), enthält die Information „2 von 2“
   −          Das Impfzertifikat einer Dosis mit einem COVID-19 Impfstoff, bei dem nur eine Dosis vorgesehen ist (Janssen), enthält die Information „1 von 1“
   −          Das Impfzertifikat einer Dosis nach einer molekularbiologisch bestätigten Infektion mit SARS-CoV-2 enthält die Information „1 von 1“
   −          Das Impfzertifikat einer weiteren Impfung enthält die Information „3 von 3“ bzw. „2 von 2“, solange der Mindestabstand von 90 Tagen zur ersten Impfserie eingehalten wurde
   −          Impfzertifikate einer weiteren Impfung (1. Dosis Janssen oder eine Dosis nach einer molekularbiologisch bestätigten Infektion mit SARS-CoV-2) enthält die Information „3 von 1“ bzw. „2 von 1“, solange der Mindestabstand von 90 Tagen zur ersten Impfserie eingehalten wurden
- Datum der Impfung (für jede erhaltene Dosis nach empfohlenem Impfschema),
- Bezeichnung des Staates, in dem die Impfung durchgeführt wurde,
- Bezeichnung des Ausstellers des Impfzertifikats,
- eindeutige Kennung des Impfzertifikats.


## QR-Code

#### Schritt 1: QR-Code Lesen
``` zbarimg klaus.jpg > code.txt ``` -- qr code lesen

##### QR-Code inhalt:
```
HC1:NCFOXN%TS3DHDWKJ/8 1K10K.0ICID:D4WGF%CM4Z4OYC5DOX-INXS6G5ZMIN9HNO4*J8OX4W$C2VL*LA:CJ/IE%TE6UG+ZEAT1HQ13W1:O1YUIPG1L+N1*PVD4WYH6IAXPMGAG5QNG.87/GYE9/MV*/R*LPLV2GHKW/F3IKJ5QH*AA:GP/HX*AO2K-0O:A0RFGK1LO%3P3M57UN92CA86:CO 20PPIE9WT0K3M9UVZSVV*001HW%8VD98-O+SQ4IJZJJ1W4*$I*NVPC1LJL4A7N832F14+KJJIU%O6QS47T0QIRR97I2HOAXL92L0B-S-*O/Y41FDLW4OMOO*3Q0K%8W%6QSC9FFFJMO:A31HJ37HZW4Q05KCTVZK7YVK.GO05 CT8OF6S41 2V7J$%25I3KC31835AL+-4J1WA6CSTU2HIJWGW7PHHDQL4*$DG2KMDBGXPP6BQFFFMCB2REXK9XUT.OLZO4Q3NZDGW1RRMKPR8X1A 9A0J%8JA5SSEM9NUH0R9MR25KCFTH1QNI96YBW40N0TJ5
```

#### Schritt 2: Entschlüsseln

```
 cat code.txt | python3 hc1_verify.py -v -i -p -A > zert.txt
```

##### Dekodierte Datei:
###### Impfzertifikat
```
Signature           : gNhlvKFJfEE= @ ES256
Experation time     : 1670972400
Issued At           : 1639498085
Issuer              : AT
Health payload      : {
    "dob": "2002-12-21",
    "nam": {
        "fn": "Scheiböck",
        "fnt": "SCHEIBOECK",
        "gn": "Klaus",
        "gnt": "KLAUS"
    },
    "v": [
        {
            "ci": "URN:UVCI:01:AT:8I5MPPGQB5JHQE5GAXNR86E8L#4",
            "co": "AT",
            "dn": 3,
            "dt": "2021-12-14",
            "is": "Ministry of Health, Austria",
            "ma": "ORG-100030215",
            "mp": "EU/1/20/1528",
            "sd": 3,
            "tg": "840539006",
            "vp": "J07BX03"
        }
    ],
    "ver": "1.3.0"
}
```
###### Genesenen Zertifikat
```
Signature           : gNhlvKFJfEE= @ ES256
Experation time     : 1661119200
Issued At           : 1646526441
Issuer              : AT
Health payload      : {
    "dob": "2002-12-21",
    "nam": {
        "fn": "SCHEIBOECK",
        "fnt": "SCHEIBOECK",
        "gn": "KLAUS MAXIMILIAN STEFAN",
        "gnt": "KLAUS<MAXIMILIAN<STEFAN"
    },
    "r": [
        {
            "ci": "URN:UVCI:01:AT:CASBQXESWIU1JYWBOICWW16XA#U",
            "co": "AT",
            "df": "2022-03-05",
            "du": "2022-08-21",
            "fr": "2022-02-22",
            "is": "Ministry of Health, Austria",
            "tg": "840539006"
        }
    ],
    "ver": "1.3.0"
}
```

#### Schritt 3: 
> Es kann nur die JSON-Payload von oben signiert werden!
```cat fakezert.txt | python3 hc1_sign.py > finishedFake.txt```

#### Schritt 4:
QR-Code erstellen -

##### Impfzertifikate:

##### Example 1 - Stim Turm
![image](https://user-images.githubusercontent.com/44428493/154083705-ba1d03b6-e0bf-41b6-ab9a-eb515303d24f.png)

##### Example 2 - Lambrechtn Siemens
![image](https://user-images.githubusercontent.com/44428493/154086682-70084c44-fc3d-4481-a7b6-7cefd58af2a3.png)

##### Genesenen Zertifikate

##### Example 1 - Schaxl Taxl
![qrcode](https://user-images.githubusercontent.com/44428493/157009306-6210a4e0-f3f4-4175-aebc-01309f03df4c.png)

## Schwachstellen

Personen müssen sich den Impfbescheid bzw. nach dem Freitesten den Genesungsbescheid selbst von der Geimeinde oder von [Gesundheit.gv.at](https://Gesundheit.gv.at) holen. Genesungsbescheid / Impfbescheid ist ein Zettel mit den generellen Informationen zur QR Code, der ausgedruckt wird. Die Mindest-Android Version der Grüner Pass app ist 7, alle anderen müssen ständig mit dem A4-Zettel herumrennen.

Zertifikate und QR Codes können leicht gefälscht werden um so einen Geimpft oder Genesen Status vorzutäuschen. Generell werden diese Zertifikate nur sehr selten wirklich wie vorgesehen mit der GreenCheck App + Ausweis überprüft obwohl auch dadurch die Echtheit / ob das Zertifikat für einen selbst ausgestellt ist nicht zu 100% garantiert werden kann. 

Eine Ausweis Kontrolle wäre insofern sinnvoll da sie zumindest feststellen kann ob eine Person ihr eigenes Zertifikat verwendet. Viele Personen werden sich nicht den Aufwand machen / fähig sein ein solches Zertifikat zu fälschen.

GreenCheck App funktioniert aktuell nur mit aktiver Internetverbindung was eine flächendeckende Überprüfung weiter erschwert.

### Schachstellen der GreenCheck App
Es ist desweiteren theoretisch möglich, über einen DNS-Server die Abfragen der GreenCheck App und der Grünenpass App umzuleiten, so dass die Zertifikate als gültig angezeigt werden.

![aud_dia2](https://user-images.githubusercontent.com/44428493/157420527-2fac890a-a0fc-4ace-ab86-0d05205a491f.png)
