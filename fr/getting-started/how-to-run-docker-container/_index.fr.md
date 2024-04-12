---
title: Comment exécuter Docker Containe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Comment exécuter le conteneur Cloud Docker Aspose.Cells. Aspose.Cells Cloud prend en charge Excel pour créer, convertir, fusionner, diviser, protéger, opération d'objet interne, etc.
weight: 100
---
 Le**Docker** La technologie est conçue pour automatiser le déploiement des applications en utilisant des conteneurs légers. Les développeurs peuvent utiliser un**Conteneur Docker** pour envelopper une application avec toutes ses bibliothèques et dépendances et tout déployer comme un seul package.

 Aspose.Cells L'équipe Cloud a publié le Docker Container sur[Centre Docker](https://hub.docker.com/r/aspose/cells-cloud) pour faciliter les utilisateurs de Docker. Les sections suivantes vous expliqueront comment exécuter des commandes Docker ou écrire une configuration dans un fichier Yaml pour l'outil de composition Docker.

## Configuration du conteneur

### Volumes requis

|Monter le chemin dans le conteneur|Description|
|:- |:- |
|C:\fonts|Dossier avec les polices, qui seront utilisées pour restituer les documents|
|C:\données|Dossier de stockage de fichiers|

### Paramètres

|Nom|Description|
|:- |:- |
|LicencePublicKey|Clé publique de la licence|
|LicencePrivateKey|Clé privée de la licence|


Si les paramètres « Licence » sont omis, l'application fonctionnera en mode d'essai.


### Exécutez un conteneur Docker en utilisant la ligne de commande

 Vous pouvez simplement exécuter la commande docker suivante après avoir extrait le conteneur de[Centre Docker](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

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
