---
title: Comment exécuter Docker Containe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Comment exécuter le conteneur Docker Aspose.Cells Cloud. Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 100
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Comment exécuter un conteneur Docker
---
 Le**Docker** Cette technologie est conçue pour automatiser le déploiement des applications grâce à l'utilisation de conteneurs légers. Les développeurs peuvent utiliser un**Conteneur Docker** pour envelopper une application avec toutes ses bibliothèques et dépendances et tout déployer sous forme de package unique.

 L'équipe Cloud Aspose.Cells a publié le conteneur Docker sur[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud)Pour faciliter la tâche des utilisateurs de Docker, les sections suivantes vous guideront dans l'exécution de commandes Docker ou l'écriture de configurations dans un fichier Yaml pour l'outil Docker Compose.

## Configuration du conteneur

### Volumes requis

|Chemin de montage dans le conteneur|Description|
|:- |:- |
|C:\polices|Dossier contenant les polices qui seront utilisées pour rendre les documents|
|C:\data|Dossier de stockage de fichiers|

### Paramètres

|Nom|Description|
|:- |:- |
|LicenceClé publique|Clé publique de la licence|
|LicenceClé privée|Clé privée de la licence|

Si les paramètres « Licence » sont omis, l'application fonctionnera en mode d'essai.

### Exécuter un conteneur Docker à l'aide de la ligne de commande

 Vous pouvez simplement exécuter la commande docker suivante après avoir extrait le conteneur de[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Configurations pour l'outil Docker-Compose

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
