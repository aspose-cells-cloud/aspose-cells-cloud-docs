---
---
title: "Come impostare la posizione di archiviazione per il contenitore Docker di Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Configurazione dell'archiviazione del contenitore Docker di Aspose.Cells Cloud"
linktitle: "Archiviazione del contenitore"
type: docs
url: /docker/storage/
description: "Configura la posizione di archiviazione per i contenitori Docker di Aspose.Cells Cloud utilizzando file JSON, PowerShell o Bash."
weight: 30
keywords: "Aspose.Cells, Docker, archiviazione contenitori, configurazione JSON, PowerShell, Bash"
---

**Sommario**: Questa guida illustra come configurare la posizione di archiviazione per i contenitori Docker di Aspose.Cells Cloud su Windows e Linux, utilizzando file di configurazione JSON e comandi `docker run`.

## Configurazione predefinita dell'archiviazione ##

**Prerequisiti**: Assicurati che Docker Engine 20.10+ sia installato, che disponi di chiavi di licenza valide per Aspose.Cells Cloud (`LicensePublicKey` e `LicensePrivateKey`) e che la cartella host che intendi utilizzare per l'archiviazione (ad esempio `c:/data` su Windows o `/data` su Linux) esista già e disponga delle autorizzazioni appropriate.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "Prima archiviazione",
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
      "Name": "Prima archiviazione",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Posizione predefinita ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Configurazione personalizzata dell'archiviazione ##

Specifica un profilo di archiviazione personalizzato quando hai bisogno di utilizzare una cartella diversa per i dati di Aspose.Cells Cloud.

```bash
docker run -d \
  -v c:/data:c:/data \   # monta la cartella host come archiviazione del contenitore
  -p 47900:5000 \        # mappa la porta dell'API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Esempio Linux*:

```bash
docker run -d \
  -v /data:/data \   # monta la cartella host come archiviazione del contenitore
  -p 47900:5000 \    # mappa la porta dell'API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Documento di riferimento**:

- [Come eseguire il contenitore Docker di Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Funzionalità del contenitore Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [Scaricare l'immagine Docker di Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/download-image/)
- [Gestire i tag del contenitore](https://docs.aspose.cloud/cells/docker/manage-tags/)