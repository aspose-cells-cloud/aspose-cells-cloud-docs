---
title: Hur man kör Docker Containe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Hur man kör Docker Aspose.Cells Molncontainer. Aspose.Cells Cloud stöder Excel för att skapa, konvertera, sammanfoga, dela, skydda, inre objektoperation och så vidare
weight: 100
---
 De**Hamnarbetare** Tekniken är utformad för att automatisera distributionen av applikationerna genom att använda lätta behållare. Utvecklare kan använda en**Docker Container** att avsluta ett program med alla dess bibliotek och beroenden och distribuera allt som ett enda paket.

 Aspose.Cells Cloud-teamet har publicerat Docker Container på[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) för att underlätta Docker-användarna. Följande avsnitt kommer att guida dig hur du kör ett Docker-kommandon eller skriver konfiguration i en Yaml-fil för Docker-skrivverktyget.

## Behållarkonfiguration

### Erforderliga volymer

|Montera banan i container|Beskrivning|
|:- |:- |
|C:\fonts|Mapp med typsnitt, som kommer att användas för att rendera dokument|
|C:\data|Fillagringsmapp|

### Parametrar

|namn|Beskrivning|
|:- |:- |
|LicensePublicKey|Licensens offentliga nyckel|
|LicensPrivateKey|Licensens privata nyckel|


Om "Licens"-parametrar utelämnas kommer appen att fungera i testläge.


### Kör en Docker-behållare med kommandoraden

 Du kan helt enkelt köra följande docker-kommando efter att ha dragit behållaren från[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Konfigurationer för Docker-Compose Tool

Du kan skriva följande konfigurationer i din yaml-fil för verktyget Docker-Compose:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
