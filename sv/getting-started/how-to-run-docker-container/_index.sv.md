---
title: Hur man kör Docker-behållaren
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Hur man kör Docker Aspose.Cells Cloud-container. Aspose.Cells Cloud stöder Excel för att skapa, konvertera, slå samman, dela, skydda, hantera interna objekt och så vidare.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hur man kör Docker-container
---
 De**Hamnarbetare** Tekniken är utformad för att automatisera distributionen av applikationerna genom att använda lättviktiga containrar. Utvecklare kan använda en**Docker-behållare** att avsluta en applikation med alla dess bibliotek och beroenden och distribuera allt som ett enda paket.

 Aspose.Cells Molnteamet har publicerat Docker-containern på[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud)för att underlätta för Docker-användare. Följande avsnitt vägleder dig i hur du kör Docker-kommandon eller skriver konfiguration i en Yaml-fil för Docker Compose-verktyget.

## Containerkonfiguration

### Nödvändiga volymer

|Monteringssökväg i container|Beskrivning|
|:- |:- |
|C:\fonter|Mapp med teckensnitt, som kommer att användas för att rendera dokument|
|C:\data|Fillagringsmapp|

### Parametrar

|Namn|Beskrivning|
|:- |:- |
|LicensOffentlig nyckel|Licensens offentliga nyckel|
|LicensPrivatnyckel|Licensens privata nyckel|

Om parametrarna "Licens" utelämnas kommer appen att fungera i testläge.

### Kör en Docker-container med hjälp av kommandoraden

 Du kan helt enkelt köra följande docker-kommando efter att du har hämtat containern från[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Konfigurationer för Docker-Compose-verktyget

Du kan skriva följande konfigurationer i din yaml-fil för Docker-Compose-verktyget:

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
