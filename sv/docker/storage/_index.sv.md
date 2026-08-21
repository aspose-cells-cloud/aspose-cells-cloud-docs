---
title: "Hur du ställer in lagringsplatsen för Aspose.Cells Cloud Docker-containerlager"
second_title: "Dokument"
ArticleTitle: "Konfiguration av Aspose.Cells Cloud Docker-containerlager"
linktitle: "Containerlager"
type: docs
url: /docker/storage/
description: "Konfigurera lagringsplatsen för Aspose.Cells Cloud Docker-containrar med JSON, PowerShell eller Bash."
weight: 30
keywords: "Aspose.Cells, Docker, containerlager, JSON-konfiguration, PowerShell, Bash"
---

**Sammanfattning**: Denna guide visar hur du konfigurerar lagringsplatsen för Aspose.Cells Cloud Docker-containrar på Windows och Linux med hjälp av JSON-konfigurationsfiler och Docker-kommandon (`docker run`).

## Standardkonfiguration för lager ##

**Förutsättningar**: Se till att Docker Engine 20.10+ är installerat, att du har giltiga Aspose.Cells Cloud-licensnycklar (`LicensePublicKey` och `LicensePrivateKey`) och att mappen på värddatorn som du planerar att använda för lagring (t.ex. `c:/data` på Windows eller `/data` på Linux) finns och har rätt behörigheter.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Standardplats ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Anpassad lagringskonfiguration ##

Använd en anpassad lagringsprofil när du behöver använda en annan mapp för Aspose.Cells Cloud-data.

```bash
docker run -d \
  -v c:/data:c:/data \   # montera värddatormappen som containerlager
  -p 47900:5000 \        # kartlägg API-porten
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Exempel för Linux*:

```bash
docker run -d \
  -v /data:/data \   # montera värddatormappen som containerlager
  -p 47900:5000 \    # kartlägg API-porten
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Referensdokument** :

- [Hur du kör Aspose.Cells Cloud Docker-container.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Funktioner för Docker-container](https://docs.aspose.cloud/cells/docker/container-features/)
- [Hämtning av Aspose.Cells Cloud Docker-avbildning](https://docs.aspose.cloud/cells/docker/download-image/)
- [Hantering av containertaggar](https://docs.aspose.cloud/cells/docker/manage-tags/)