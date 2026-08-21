---
title: "Comment exécuter le conteneur Docker Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Comment exécuter le conteneur Docker Aspose.Cells Cloud"
linktype: "Container Run"
type: docs
url: /fr/run-aspose-cells-cloud-docker-container/
description: "Découvrez comment lancer Aspose.Cells Cloud dans un conteneur Docker sur Windows Server 2022. Commandes détaillées étape par étape pour les modes d'essai, de facturation au usage (metered), de facturation par licence, la configuration du stockage et la vérification de santé."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, mode d'essai, facturation au usage, facturation par licence, configuration du stockage"
---

Aspose.Cells Cloud Docker fournit une image de conteneur prête à l'emploi qui héberge localement ou dans un cloud privé l’API Aspose.Cells Cloud. Ce guide explique comment démarrer le conteneur selon trois modes de licence courants : **Essai**, **Facturation au usage** et **Facturation par licence**, ainsi qu’une variante utilisant un jeton d’accès. Toutes les commandes sont conçues pour PowerShell sur Windows Server 2022 ; adaptez les chemins de volumes si vous utilisez Linux.

**Prérequis**

- Docker Engine 20.10 ou version ultérieure installé et en cours d’exécution.  
- PowerShell 5.1 ou PowerShell 7+.  
- Port 5000 ouvert à l’intérieur du conteneur (mappé au port hôte 47900) et pare-feu hôte autorisant le trafic entrant sur le port 47900.  
- Pour les modes de facturation au usage ou par licence, disposer de la `LicensePublicKey`, de la `LicensePrivateKey` ou d’un fichier de licence, ou d’un `AccessToken` si le mode par jeton est utilisé.  
- Un dossier local (par exemple `C:\data`) à monter en tant que stockage pour le conteneur.

**Démarrage rapide (mode d’essai)**  

Exécutez la commande suivante pour lancer le conteneur en mode d’essai :

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Exécuter le conteneur Docker Aspose.Cells Cloud en mode d’essai

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Le conteneur s’exécute en premier plan et écoute sur le port hôte **47900**, qui redirige vers le port interne **5000** du conteneur.

## Exécuter le conteneur Docker Aspose.Cells Cloud en mode de facturation au usage

```powershell
# Windows Server 2022
# Mode de facturation au usage : définir LicensePublicKey et LicensePrivateKey en tant que variables d’environnement.
# Monter un dossier de stockage (hôte → conteneur)
#   -v c:/data:c:/data
# Monter le dossier des polices Windows afin que l’API puisse y accéder
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=votreClePublique `
  -e LicensePrivateKey=votreClePrivee `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Le conteneur s’exécute en mode détaché (`-d`). Une fois lancé, vous pouvez vérifier que le service est accessible :

```powershell
curl http://localhost:47900/v3.0/health
```

**Exemple de fichier `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Exécuter le conteneur Docker Aspose.Cells Cloud en mode de facturation par licence

```powershell
# Windows Server 2022
# Mode de facturation par licence : fournir un fichier de licence via la variable d’environnement LicenseFile.
# Monter un dossier de stockage (hôte → conteneur)
#   -v c:/data:c:/data
# Monter le dossier des polices Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Exécuter le conteneur Docker Aspose.Cells Cloud avec un jeton d’accès

```powershell
# Windows Server 2022
# Mode par jeton d’accès : définir AccessToken, éventuellement combiné aux clés de facturation au usage.
# Monter un dossier de stockage
#   -v c:/data:c:/data
# Monter le dossier des polices Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=votreClePublique `
  -e LicensePrivateKey=votreClePrivee `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Après le lancement du conteneur, confirmez que le service est opérationnel à l’aide de la même commande de vérification de santé mentionnée précédemment.

## Document de référence

- [Comment configurer le stockage du conteneur Docker Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Dépannage

- **Échec de la vérification de santé** – Vérifiez que le port 47900 n’est pas bloqué par un pare-feu et que le conteneur est bien en cours d’exécution (`docker ps`).  
- **Erreurs de licence** – Vérifiez que les valeurs `LicensePublicKey`, `LicensePrivateKey` ou `LicenseFile` sont correctes et que les variables d’environnement sont transmises sans espaces superflus.  
- **Stockage inaccessible** – Assurez-vous que le dossier hôte (`c:/data`) existe et que Docker dispose des autorisations de lecture/écriture dessus.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Comment exécuter le conteneur Docker Aspose.Cells Cloud",
  "description": "Guide étape par étape pour lancer Aspose.Cells Cloud dans un conteneur Docker sur Windows Server 2022, couvrant les modes d’essai, de facturation au usage, de facturation par licence et de jeton d’accès.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, mode d'essai, facturation au usage, facturation par licence, configuration du stockage"
}
</script>