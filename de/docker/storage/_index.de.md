---
title: "So legen Sie die Speicherposition für den Aspose.Cells Cloud Docker-Container fest"
second_title: "Dokument"
ArticleTitle: "Konfiguration des Aspose.Cells Cloud Docker-Container-Speichers"
linktitle: "Container-Speicher"
type: docs
url: /docker/storage/de/
description: "Konfigurieren Sie den Speicherort für Aspose.Cells Cloud Docker-Container mithilfe von JSON, PowerShell oder Bash."
weight: 30
keywords: "Aspose.Cells, Docker, Container-Speicher, JSON-Konfiguration, PowerShell, Bash"
---

**Zusammenfassung**: Dieser Leitfaden zeigt, wie Sie den Speicherort für Aspose.Cells Cloud Docker-Container unter Windows und Linux mithilfe von JSON-Konfigurationsdateien und Docker-`run`-Befehlen konfigurieren.

## Standard-Speicherkonfiguration ##

**Voraussetzungen**: Stellen Sie sicher, dass Docker Engine 20.10+ installiert ist, Sie über gültige Aspose.Cells Cloud-Lizenzschlüssel (`LicensePublicKey` und `LicensePrivateKey`) verfügen und der Host-Ordner, den Sie für den Speicher verwenden möchten (z. B. `c:/data` unter Windows oder `/data` unter Linux), mit entsprechenden Berechtigungen vorhanden ist.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "Erster Speicher",
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
      "Name": "Erster Speicher",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Standardposition ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Benutzerdefinierte Speicherkonfiguration ##

Geben Sie ein benutzerdefiniertes Speicherprofil an, wenn Sie einen anderen Ordner für Aspose.Cells Cloud-Daten verwenden möchten.

```bash
docker run -d \
  -v c:/data:c:/data \   # Host-Ordner als Container-Speicher einbinden
  -p 47900:5000 \        # API-Port zuweisen
  -e LicensePublicKey=IhrLicensePublicKey \
  -e LicensePrivateKey=IhrLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux-Beispiel*:

```bash
docker run -d \
  -v /data:/data \       # Host-Ordner als Container-Speicher einbinden
  -p 47900:5000 \        # API-Port zuweisen
  -e LicensePublicKey=IhrLicensePublicKey \
  -e LicensePrivateKey=IhrLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Referenzdokumentation**:

- [So führen Sie den Aspose.Cells Cloud Docker-Container aus.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Funktionen des Docker-Containers](https://docs.aspose.cloud/cells/docker/container-features/)
- [Herunterladen des Aspose.Cells Cloud Docker-Images](https://docs.aspose.cloud/cells/docker/download-image/)
- [Verwalten von Container-Tags](https://docs.aspose.cloud/cells/docker/manage-tags/)