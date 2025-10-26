---
title: "Comment exécuter le conteneur Cloud Docker Aspose.Cells : exécutez le conteneur Cloud officiel Aspose.Cells en 3 étapes : extraction, configuration, démarrage"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /fr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Comment exécuter le conteneur Docker Aspose.Cells Cloud. Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Comment exécuter un conteneur Docker
---
 Le**Docker** La technologie est conçue pour automatiser le déploiement des applications grâce à l'utilisation de conteneurs légers. Les développeurs peuvent utiliser un**Conteneur Docker** pour envelopper une application avec toutes ses bibliothèques et dépendances et tout déployer sous forme de package unique.

 L'équipe Cloud Aspose.Cells a publié le conteneur Docker sur[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) Pour faciliter la tâche des utilisateurs de Docker, les sections suivantes vous guideront dans l'exécution de commandes Docker ou l'écriture de configurations dans un fichier Yaml pour l'outil Docker Compose.

## Configuration du conteneur

### Volumes requis

|Chemin de montage dans le conteneur|Description|
|:- |:- |
|C:\polices|Dossier contenant les polices, qui seront utilisées pour restituer les documents|
|C:\données|Dossier de stockage de fichiers|

### Paramètres

|Nom|Description|
|:- |:- |
|LicenceClé publique|Clé publique de la licence|
|LicenceClé privée|Clé privée de la licence|

Si les paramètres « Licence » sont omis, l'application fonctionnera en mode d'essai.

### 1. Extraire l'image du nuage Aspose.Cells

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Configurations pour l'outil Docker-Compose

Vous pouvez écrire les configurations suivantes dans votre fichier yaml pour l'outil Docker-Compose :

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

### 3. Exécutez un conteneur Docker à l'aide de la ligne de commande

 Vous pouvez simplement exécuter la commande Docker suivante après avoir extrait le conteneur de[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
