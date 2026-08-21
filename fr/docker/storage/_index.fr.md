---
title: "Comment définir la position de stockage pour le conteneur Docker Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Configuration du stockage Docker Aspose.Cells Cloud"
linktype: "docs"
url: /fr/docker/storage/
description: "Configurez l’emplacement de stockage des conteneurs Docker Aspose.Cells Cloud à l’aide de fichiers JSON, PowerShell ou Bash."
weight: 30
keywords: "Aspose.Cells, Docker, stockage de conteneur, configuration JSON, PowerShell, Bash"
---

**Résumé** : Ce guide explique comment configurer l’emplacement de stockage des conteneurs Docker Aspose.Cells Cloud sur Windows et Linux à l’aide de fichiers de configuration JSON et des commandes Docker run.

## Configuration de stockage par défaut ##

**Prérequis** : Assurez-vous que Docker Engine 20.10 ou une version ultérieure est installé, que vous disposez de clés de licence valides pour Aspose.Cells Cloud (`LicensePublicKey` et `LicensePrivateKey`), et que le dossier hôte que vous comptez utiliser comme stockage (par exemple `c:/data` sous Windows ou `/data` sous Linux) existe et dispose des autorisations appropriées.

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

## Emplacement par défaut ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Configuration personnalisée du stockage ##

Spécifiez un profil de stockage personnalisé si vous souhaitez utiliser un dossier différent pour les données d’Aspose.Cells Cloud.

```bash
docker run -d \
  -v c:/data:c:/data \   # montage du dossier hôte en tant que stockage du conteneur
  -p 47900:5000 \        # mappage du port de l’API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Exemple Linux* :

```bash
docker run -d \
  -v /data:/data \   # montage du dossier hôte en tant que stockage du conteneur
  -p 47900:5000 \    # mappage du port de l’API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Document de référence** :

- [Comment exécuter un conteneur Docker Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Fonctionnalités des conteneurs Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [Téléchargement de l’image Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/download-image/)
- [Gestion des balises de conteneur](https://docs.aspose.cloud/cells/docker/manage-tags/)
---