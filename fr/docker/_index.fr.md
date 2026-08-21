---
title: "Manuel d’exploitation Aspose.Cells Cloud Docker : héberger l’application Aspose.Cells Cloud sur votre propre infrastructure privée."
second_title: "Document"
ArticleTitle: "Manuel d’exploitation Aspose.Cells Cloud Docker"
linktype: "docs"
url: /fr/docker-developer-guide/
aliases: [  /fr/docker/ , /fr/docker/run/ ]
description: "Déployer Aspose.Cells Cloud en tant que conteneur Docker sur une infrastructure privée ou locale, permettant le traitement de feuilles de calcul (Excel, PDF, CSV, JSON, Markdown) sans recourir au cloud public d’Aspose."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Image Docker",
    "API de feuilles de calcul",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Cloud privé",
    "Déploiement",
  ]
weight: 30
---

Aspose.Cells Cloud est un service de traitement de feuilles de calcul basé sur le cloud, prenant en charge la création, l’édition, la conversion et la manipulation de fichiers dans des formats tels qu’Excel. Il peut être rapidement mis en place comme environnement de service autonome via un déploiement Docker, simplifiant ainsi la gestion des dépendances et les processus de déploiement multiplateforme.

Ce manuel fournit une présentation détaillée de l’ensemble des étapes opérationnelles, depuis la préparation de l’environnement jusqu’à la vérification du service.

## Préparation de l’environnement

Avant de déployer le conteneur Docker Aspose.Cells Cloud, assurez-vous que l’environnement local répond aux exigences de dépendances suivantes afin d’éviter les échecs de déploiement dus à des composants manquants.

### Composants de dépendance de base

- **Docker Engine :** Moteur principal d’exécution des conteneurs, responsable de la création et de la gestion des conteneurs. Version minimale requise : **18.09.0**.
- **Systèmes d’exploitation :** Principaux systèmes d’exploitation prenant en charge Docker

  | Type de système d’exploitation | Version                   |
  | :------------------------------ | :------------------------ |
  | Windows                         | Windows 10/11             |
  | Windows Server                  | 2016 / 2019 / 2022        |
  | Linux                           | CentOS 7+ / Ubuntu 20.04+ |

- **Ressources matérielles :** Assurez-vous que les ressources suffisantes sont disponibles pour éviter les pannes dues à un manque de capacités.
  - CPU : 2 cœurs ou plus.
  - Mémoire : 4 Go ou plus.
  - Disque : 10 Go d’espace libre.

### Conditions préalables essentielles

- **Licence Aspose :** Inscrivez-vous à un compte officiel Aspose afin d’obtenir une licence valide (vous pouvez demander une version d’essai ou acheter une version commerciale). Sans licence, les fonctionnalités du service pourraient être limitées. Veuillez consulter la page [Licence](https://purchase.aspose.com/buy) pour plus de détails.
- **Connectivité réseau :** Assurez-vous que l’environnement de déploiement peut accéder à Docker Hub (afin de télécharger les images).

## Télécharger l’image Docker Aspose.Cells Cloud

L’image Aspose.Cells Cloud est hébergée sur Docker Hub et peut être récupérée directement à l’aide de la commande `docker pull`, sans nécessiter de construction manuelle.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Exécuter le conteneur Docker Aspose.Cells Cloud

### Paramètres d’exécution

| Nom                           | Description                                                                 | Remarque                                                     |
| ----------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey              | Définir la clé publique de la licence lors de l’utilisation du mode de facturation basé sur la consommation (Metered). | Uniquement effectif en cas d’utilisation du mode de facturation Metered. |
| LicensePrivateKey             | Définir la clé privée de la licence lors de l’utilisation du mode de facturation basé sur la consommation (Metered). | Uniquement effectif en cas d’utilisation du mode de facturation Metered. |
| storagesCredentialsFilePath   | Chemin vers le fichier de configuration de stockage. Le fichier par défaut est `./storageResource.json`. |                                                              |
| LicenseFile                   | Définir le fichier de licence lors de l’utilisation du mode de facturation LicenseFile. | Uniquement effectif en cas d’utilisation du mode de facturation LicenseFile. |
| AccessToken                   | Jeton d’accès à l’API.                                                      | Si vide, aucune vérification par jeton n’est requise.       |

### Commande d’exécution

Lancer le conteneur en mode d’essai est aussi simple que cela :

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Pour une exécution complète dotée de toutes les fonctionnalités, obtenez une [licence Metered](https://purchase.aspose.com/faqs/licensing/metered/) et montez un dossier hôte pour le stockage des fichiers. Voici à quoi ressemble la commande d’exécution dans ce cas :

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### Référence API – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Exposition du port

| Port | Description                                          | Obligatoire |
| ---- | ---------------------------------------------------- | ----------- |
| 5000 | Dossier contenant les polices utilisées pour le rendu des documents | Oui         |

### Volumes requis

| Chemin de montage dans le conteneur | Description                                          | Obligatoire | Remarque                                                       |
| ----------------------------------- | ---------------------------------------------------- | ----------- | -------------------------------------------------------------- |
| C:\fonts                            | Dossier contenant les polices utilisées pour le rendu des documents | Non         | Résout les problèmes de feuilles de calcul/Excel causés par des polices manquantes. |
| C:\data                             | Dossier de stockage des fichiers                     | Non         | Augmente l’espace de stockage pour une gestion et un accès plus simples aux fichiers. |

## Documentation de référence

- [Fonctionnalités principales du conteneur Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker-container-features/)
- [Comment configurer le stockage du conteneur Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/storage/)
- [Comment exécuter le conteneur Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)