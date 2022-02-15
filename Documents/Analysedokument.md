Anforderungen: 

* 4 Seiten
* Funktionsweise des aktuellen Systems (inkl. Architektur und Sequenzdiagramm)
* QR-Code (Inhatl, Generierung und Verifizierung)
* Schwachstellen (digital/analog)

# Analysedokument 

*Gruppe Aigner, Wimmer, Scheiböck, Mayr und Aspöck*

## Funktionsweise des aktuellen Systems

![image](https://user-images.githubusercontent.com/44428493/154077280-325734ce-d0c9-4433-8123-3ad4eedf71cd.png)


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

#### Schritt 3: 
> Es kann nur die JSON-Payload von oben signiert werden!
```cat fakezert.txt | python3 hc1_sign.py > finishedFake.txt```

#### Schritt 4:
QR-Code erstellen - ![image](https://user-images.githubusercontent.com/44428493/154083705-ba1d03b6-e0bf-41b6-ab9a-eb515303d24f.png)


## Schwachstellen

